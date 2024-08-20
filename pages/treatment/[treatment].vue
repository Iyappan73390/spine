<template>
    <Header />
    <div class="container mt-3">
        <a href="#" onclick="history.back()" class="backbtn"><span
                class="material-symbols-outlined">keyboard_backspace</span> Back</a>
        <div class="row mt-3">
            <div class="col-md-12">
                <div class="treatmentbnr">
                    <img :src="`https://templates.mocerohealth.in${treatment?.attributes?.image?.data?.attributes?.url}`"
                        alt="" class="img-fluid treatmentimg">
                    <div class="treatmentbnrcontent">
                        <div class="treattitle">
                            <h5>{{ treatment.attributes.title }}</h5>
                        </div>
                        <p>{{ treatment.attributes.description }}</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="row">
            <div v-if="convertedtreatmentcontent" v-html="convertedtreatmentcontent" class="my-5"></div>
        </div>

        <div class="row mb-5">
            <div class="row" v-if="treatment.attributes.diagnosis && treatment.attributes.diagnosis.length > 0">
                <h3 class="mb-4"><b>Diagnosis</b></h3>
            </div>
            <div class="row" v-if="treatment.attributes.diagnosis && treatment.attributes.diagnosis.length > 0">
                <div class="col-lg-4 col-md-6 col-sm-12 col-xs-12 mb-3" v-for="diagnosis in treatment.attributes.diagnosis" :key="diagnosis.id">
                    <div class="diagnosissec">
                        <div>
                        <h5><b>{{ diagnosis.title }}</b></h5>
                        <ul>
                            <li v-for="listItem in diagnosis.list" :key="listItem.id">{{ listItem.name }}</li>
                        </ul>
                    </div>
                    <img :src="`https://templates.mocerohealth.in/${diagnosis.image.data.attributes.url}`" :alt="diagnosis.image.data.attributes.alternativeText || diagnosis.title">
                    </div>
                </div>
            </div>
        </div>


        <div class="row mb-5">
            <div class="row" v-if="blogdata && blogdata.length > 0">
                <h3 class="mb-4"><b>Realted Blogs</b></h3>
            </div>
            <div class="row" v-if="blogdata && blogdata.length > 0">
                <div class="col-lg-4 col-md-6 col-sm-12 col-xs-12 mb-3" v-for="blog in blogdata" :key="blog.id">
                    <div class="blogcard">
                        <nuxt-link :to="`/blogs/${blog.attributes?.slug}`">
                            <img :src="`https://templates.mocerohealth.in${blog.attributes?.blog_card?.image?.data?.attributes?.url}`"
                                alt="">
                            <h3>{{ blog.attributes.blog_card.title }}</h3>
                            <span>{{ blog.attributes.blog_card.category }}</span>
                            <p>{{ blog.attributes.blog_card.description }}</p>
                            <a href="#" class="readmore">Read more <i class="fa fa-angle-right" aria-hidden="true"></i></a>
                        </nuxt-link>
                    </div>
                </div>
            </div>
        </div>

        <div class="row my-5">
            <div class="accordion" v-for="faq in treatment.attributes.faq" :key="faq.id">
                <div class="accordion-item">
                    <button id="accordion-button-1" aria-expanded="false"><span class="accordion-title">{{ faq.question }}</span><span class="icon" aria-hidden="true"></span></button>
                    <div class="accordion-content">
                        <p>{{ faq.answer }}</p>
                    </div>
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
const treatmentData = await useFetch(`https://templates.mocerohealth.in/api/treatments/${slug.treatment}`);
const treatment = treatmentData.data._rawValue.data;

const blogdata = treatment.attributes.blogs.data

const convertedtreatmentcontent = ref('');

onMounted(() => {
    if (typeof window !== 'undefined') {
        const converter = new window.showdown.Converter();
        convertedtreatmentcontent.value = converter.makeHtml(treatment?.attributes?.treatment_content);
    }

    const items = document.querySelectorAll(".accordion button");

    function toggleAccordion() {
        const itemToggle = this.getAttribute('aria-expanded');
        
        for (let i = 0; i < items.length; i++) {
            items[i].setAttribute('aria-expanded', 'false');
        }
        
        if (itemToggle == 'false') {
            this.setAttribute('aria-expanded', 'true');
        }
    }

    items.forEach(item => item.addEventListener('click', toggleAccordion));
});
</script>

<style scoped>

.treatmentbnr {
    width: 100%;
    height: 500px;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
}

.treatmentbnr img {
    width: 100%;
    height: 100%;
}
.treatmentimg{
    border-radius: 10px;
}
.treatmentbnr .treatmentbnrcontent {
    position: absolute;
    top: 45%;
}

.treatmentbnr .treatmentbnrcontent .treattitle {
    padding: 10px;
    color: #444444;
    background: #fff;
    margin-bottom: 20px;
}

.treatmentbnr .treatmentbnrcontent .treattitle h5 {
    font-weight: 600;
    margin-bottom: 0;
    text-align: center;
    font-size: 35px;
}

.treatmentbnr .treatmentbnrcontent p {
    color: #fff;
}
.diagnosissec{
    display: flex;
    align-items: center;
    justify-content: space-between;
    border: 1px solid #e1e1e1;
    padding: 15px;
    border-radius: 5px;
}
.diagnosissec h5{
    color: #000000;
    font-size: 16px;
}
.diagnosissec ul li{
    color: #999999;
}
.diagnosissec img{
    width: 120px;
    height: 120px;
}
</style>
