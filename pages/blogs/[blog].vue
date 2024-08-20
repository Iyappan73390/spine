<template>
  <Header />
    <section class="bannerimg">
      <img v-if="blogs?.attributes?.blog_card?.image?.data?.attributes?.url" :src="`https://templates.mocerohealth.in/${blogs?.attributes?.blog_card?.image?.data?.attributes?.url}`" alt="">
      <div v-else class="dummyimg"></div>
    </section>
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <div v-if="convertedblogcontent" v-html="convertedblogcontent" class="my-5 blogcontent"></div>
        </div>
      </div>
    </div>

    <!-- RELATED BLOGS -->
     <div class="container">
        <div class="row" v-if="relatedblogs && relatedblogs.length > 0">
          <h3><b>Related Blogs</b></h3>
        </div>
        <div class="row" v-if="relatedblogs && relatedblogs.length > 0">
                <div class="col-md-4 col-sm-6 col-xs-12 my-3" v-for="relatedblog in relatedblogs" :key="relatedblog.id">
                    <div class="blogcard">
                    <nuxt-link :to="`/blogs/${relatedblog.attributes?.slug}`">
                            <img v-if="relatedblog.attributes?.blog_card?.image?.data?.attributes?.url" :src="`https://templates.mocerohealth.in${relatedblog.attributes?.blog_card?.image?.data?.attributes?.url}`" alt="">
                              <div v-else class="dummmyimg"></div>
                            <h3>{{ relatedblog.attributes.blog_card.title }}</h3>
                            <span>{{ relatedblog.attributes.blog_card.category }}</span>
                            <p>{{ relatedblog.attributes.blog_card.description }}</p>
                            <a href="#" class="readmore">Read more <i class="fa fa-angle-right" aria-hidden="true"></i></a>
                    </nuxt-link>
                    </div>
                </div>
            </div>
     </div>
    <Footer />
  </template>
  
  <script setup>
  import { ref, onMounted } from 'vue';
  import { useRoute } from 'vue-router';

  useHead({
  title: 'SS Spine & Ortho Clinic'
})
  
  const slug = useRoute().params;
  
  const blogData = await useFetch(`https://templates.mocerohealth.in/api/blogs/${slug.blog}`);
  const blogs = blogData.data._rawValue.data; // Adjust this line according to the actual structure of your data

  const relatedblogs = blogs.attributes.blogs.data;


console.log(blogs);
  
  const convertedblogcontent = ref('');
  
  onMounted(() => {
    if (typeof window !== 'undefined') {
      const converter = new window.showdown.Converter();
      convertedblogcontent.value = converter.makeHtml(blogs?.attributes?.blogcontent);
    }
  });
  </script>
  
  <style scoped>
  .bannerimg {
    width: 100%;
    height: 70vh;
  }
  .bannerimg img {
    width: 100%;
    height: 100%;
  }
  .dummmyimg{
    width: 100%;
    height: 100%;
  }
  .dummyimg{
    width: 100%;
    height: 60vh;
    background-color: #e5e5e5;
  }
  </style>
  