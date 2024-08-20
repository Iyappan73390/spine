<template>
    <Header />
    <section class="bannersec">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-md-6 col-sm-12">
                    <h2>Spinal Conditions</h2>
                    <p class="mb-100">Low back pain is extremely common problem that most of us will experience at some point in their life time. About 
                        8 in 10 people have one or more episodes of low back pain. In most cases</p>

                    <a href="/book-an-appointment" class="bookbtn">Book an Appointment <i class="fa fa-angle-right"
                            aria-hidden="true"></i></a>
                </div>
                <div class="col-md-6 col-sm-12 d-flex justify-content-center">
                    <img src="/assets/image/diseasebnr.png" class="img-fluid diseaseimg" alt="Disease image">
                </div>
            </div>
        </div>
    </section>

    <div class="container">
        <div class="row">
            <div class="col-md-12 my-5">
                <div class="our-treatmentsec">
                    <h3>Our Disease</h3>
                    <p>Our medical team is comprised of some of the finest doctors in the region, renowned for their
                        clinical expertise and innovative approaches to medicine.</p>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="diseasecards pt-4 pb-5">

                <div class="diseasecard" v-for="disease in diseasedata" :key="disease.id">
                    <nuxt-link :to="`/disease/${disease.attributes?.slug}`">
                        <img :src="`https://templates.mocerohealth.in${disease.attributes?.image?.data?.attributes?.url}`" alt="">
                        <div class="diseasecarddetail">
                            <div class="my-3">
                                <h5>{{ disease.attributes.title }}</h5>
                                <span class="material-symbols-outlined">arrow_outward</span>
                            </div>
                            <p>{{ disease.attributes.description }}</p>
                        </div>
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

    let disease = await useFetch('https://templates.mocerohealth.in/api/diseases?populate=image');
    let diseasedata = disease.data._rawValue.data
    console.log(diseasedata);

</script>


<style>
.bannersec {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgb(240,243,250);
    background: linear-gradient(103deg, rgba(240,243,250,1) 7%, rgba(145,152,160,1) 100%, rgba(145,152,160,1) 100%);
}

.bannersec h2 {
    color: #164A87;
    font-weight: 700;
    font-size: 40px;
}
.diseaseimg{
    width: 70%;
}
.our-treatmentsec {
    text-align: center;
}

.our-treatmentsec h3 {
    color: #444444;
    font-weight: 500;
}

.our-treatmentsec p {
    color: #999999;
}

@media only screen and (max-width: 868px) {
    .bannersec {
        padding-top: 50px;
    }
}
</style>