<template>
    <Header />
    <section class="bgimg">
        <div class="container">
            <div class="row text-center">
                <h1>Blogs</h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Distinctio officiis adipisci quas pariatur
                    mollitia hic tempore.
                    Ullam commodi optio ab mollitia iusto accusamus temporibus modi nisi! Nostrum cupiditate neque
                    officiis?</p>
            </div>
        </div>
    </section>
    <div class="container my-5">
            <div class="row">
                <div class="col-md-4 col-sm-6 col-xs-12 my-3" v-for="blog in blogdata" :key="blog.id">
                    <div class="blogcard">
                    <nuxt-link :to="`/blogs/${blog.attributes?.slug}`">
                            <img v-if="blog.attributes?.blog_card?.image?.data?.attributes?.url" :src="`https://templates.mocerohealth.in${blog.attributes?.blog_card?.image?.data?.attributes?.url}`" alt="">
                            <div v-else class="dummmyimg"></div>
                            <h3>{{ blog.attributes.blog_card.title }}</h3>
                            <span>{{ blog.attributes.blog_card.category }}</span>
                            <p>{{ blog.attributes.blog_card.description }}</p>
                            <a href="#" class="readmore">Read more <i class="fa fa-angle-right" aria-hidden="true"></i></a>
                    </nuxt-link>
                    </div>
                </div>
            </div>
        </div>
        <Footer />
</template>


<script setup>

useHead({
  title: 'SS Spine & Ortho Clinic'
})

    let blogs = await useFetch('https://templates.mocerohealth.in/api/blogs?populate=blog_card.image');
    debugger
    let blogdata = blogs.data._rawValue.data
    console.log(blogdata);

</script>

<style scoped>
.bgimg {
    /* background: linear-gradient(rgba(151, 142, 250, 0.8), rgba(74, 104, 146, 0.8)) fixed, url(/assets/image/images.jfif) fixed;
     */
    background: linear-gradient(to top, rgba(74, 104, 146, 0.8), rgba(38, 78, 147, 0.651)) fixed, url(/assets/image/blog_bnr.png) fixed;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    width: 100%;
    height: 70vh;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #fff;
}
.bgimg h1{
    font-weight: 700;
    font-size: 75px;
}
.dummmyimg{
    width: 100%;
    height: 300px;
    background-color: #e5e5e5;
    border-radius: 10px;
}
</style>