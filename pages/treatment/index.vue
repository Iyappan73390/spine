<template>
    <Header />
    <section class="bannersec">
        <div class="container">
            <div class="row">
                <div class="col-md-6 col-sm-12">
                    <h2>Treatments & Services</h2>
                    <p class="mb-100">Expertise in Spine & Orthopaedic care and helping you lead an active life.</p>

                    <a href="/book-an-appointment" class="bookbtn">Book an Appointment <i class="fa fa-angle-right"
                            aria-hidden="true"></i></a>
                </div>
                <div class="col-md-6 col-sm-12">
                    <img src="/assets/image/treatment_bnr.png" class="treatmentimg img-fluid" alt="treatment image">
                </div>
            </div>
        </div>
    </section>

    <div class="container">
        <div class="row">
            <div class="col-md-12 my-5">
                <div class="our-treatmentsec">
                    <h3>Our Treatments</h3>
                    <p>Our medical team is comprised of some of the finest doctors in the region, renowned for their
                        clinical expertise and innovative approaches to medicine.</p>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="treatmentCards pt-4 pb-5">
                <div class="treatmentCard" v-for="treatment in treatmentdata" :key="treatment.id">
                    <nuxt-link :to="`/treatment/${treatment.attributes?.slug}`">
                        <img :src="`https://templates.mocerohealth.in${treatment.attributes?.image?.data?.attributes?.url}`" alt="">
                        <h5>{{ treatment.attributes?.title }}</h5>
                        <p>{{ treatment.attributes?.description }}</p>
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

    let treatment = await useFetch('https://templates.mocerohealth.in/api/treatments?populate=image');
    debugger;
    let treatmentdata = treatment.data._rawValue.data
    console.log(treatmentdata);

</script>


<style>
.bannersec {
    position: relative;
    width: 100%;
    height: 70vh !important;
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgb(220, 249, 255);
    background: linear-gradient(103deg, rgba(220, 249, 255, 1) 4%, rgba(143, 212, 225, 1) 58%, rgba(143, 212, 225, 1) 100%);
}

.treatmentimg {
    position: absolute;
    right: 0;
    bottom: 0;
    width: 50%;
}

.bannersec h2 {
    color: #164A87;
    font-weight: 700;
    font-size: 40px;
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
        align-items: unset;
        padding: 30px 0px;
    }
}
</style>