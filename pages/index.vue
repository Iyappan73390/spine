<template>
  <Header />

  <div class="carousel slide home-carousel" id="carouselExampleIndicators" data-bs-ride="carousel">
    <div class="carousel-indicators">
      <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active"
        aria-current="true" aria-label="Slide 1"></button>
      <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1"
        aria-label="Slide 2"></button>
      <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2"
        aria-label="Slide 3"></button>
    </div>
    <div class="carousel-inner">

      <div class="carousel-item active" id="slide1">
        <div class="slide1">
          <div class="container">

            <div class="row">
              <div class="col-sm-6">
                <div class="slide1-cnt">
                  <h1 class="fw-bold">SS SPINE & <br>ORTHO CLINIC</h1>
                  <p class="pt-4 mb-5">The spinal cord extends from the skull to your lower back and travels through the
                    middle part of each stacked vertebra, called the central canal.</p>
                  <a href="/book-an-appointment" class="blueButton color-changing-button">Book an Appointment</a>
                </div>
              </div>
              <div class="col-sm-6">
                <img src="/assets/image/slide1.png" alt="" class="slideImage" />
              </div>
            </div>

          </div>
        </div>
        <video autoplay loop muted plays-inline="">
          <source src="" type="video/mp4">
        </video>
      </div>

      <div class="carousel-item" id="slide2">
        <div class="slide2">
          <div class="container">

            <div class="row">
              <div class="col-sm-6">
                <div class="slide2-cnt">
                  <h1 class="fw-bold">SS SPINE & <br>ORTHO CLINIC</h1>
                  <p class="pt-4 mb-5">The spinal cord extends from the skull to your lower back and travels through the
                    middle part of each stacked vertebra, called the central canal.</p>
                  <a href="/book-an-appointment" class="blueButton color-changing-button">Book an Appointment</a>
                </div>
              </div>
              <div class="col-sm-6">
                <img src="/assets/image/slide2.png" alt="" class="slideImage" />
              </div>
            </div>

          </div>
        </div>
        <video autoplay loop muted plays-inline="">
          <source src="" type="video/mp4">
        </video>
      </div>

      <div class="carousel-item" id="slide3">
        <div class="slide3">
          <div class="container">

            <div class="row">
              <div class="col-sm-6">
                <div class="slide3-cnt">
                  <h1 class="fw-bold">SS SPINE & <br>ORTHO CLINIC</h1>
                  <p class="pt-4 mb-5">The spinal cord extends from the skull to your lower back and travels through the
                    middle part of each stacked vertebra, called the central canal. </p>
                  <a href="/book-an-appointment" class="blueButton color-changing-button">Book an Appointment</a>
                </div>
              </div>
              <div class="col-sm-6">
                <img src="/assets/image/slide3.png" alt="" class="slideImage" />
              </div>
            </div>

          </div>
        </div>
        <video autoplay loop muted plays-inline="">
          <source src="" type="video/mp4">
        </video>
      </div>

    </div>

    <div class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </div>
    <div class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </div>

  </div>

  <div class="docIntro">
    <div class="container">
      <div class="row">
        <div class="col-sm-6">
          <div class="introImgSec">
            <img src="/assets/image/doctor.png" alt="" class="introImg" />
          </div>
        </div>
        <div class="col-sm-6">
          <div class="introCnt">
            <h4 class="fw-bold">Dr. Shanmugasundaram</h4>
            <p>
              M.S Ortho (JIPMER), Fellow in Spine Surgery (Hallym University, Seoul) Endoscopic Spine Surgeon;
              Consultant Spine & Ortho Surgeon
            </p>
            <br>
            <p class="mb-5">
              Dr. Shanmugasundaram is a leading spine surgeon and a Professor of Orthopaedics. With a Masters in
              Orthopaedics from JIPMER, Pondicherry, and a fellowship from Hallym University, Seoul, South Korea, his
              expertise lies in orthopaedic and spinal surgeries. He has also published numerous publications related to
              Spine & Orthopaedics and is a regular speaker at multiple national and international forums. He is also
              part of the Indian Association of Orthopaedics and the Indian Medical Association.
            </p>
            <nuxt-link to="/doctor" class="transparentButtonBlue">View More</nuxt-link>
          </div>
        </div>
      </div>
    </div>
    <a href="#" class="squareButton sideBtn">Book an Appointment</a>
  </div>

  <div class="container text-center py-5">
    <div class="descriptionSec">
      <h3 class="fw-bold">Treatments</h3>
      <p class="greyText">
        Our medical team is comprised of some of the finest doctors in the region, renowned for their clinical expertise
        and innovative approaches to medicine.
      </p>
    </div>
  </div>

  <div class="greyBg">
    <div class="container py-5">
      <div class="treatmentCards pt-4 pb-5">

        <div class="treatmentCard" v-for="treatment in treatmentdata" :key="treatment.id">
          <nuxt-link :to="`/treatment/${treatment.attributes?.slug}`">
            <img :src="`https://templates.mocerohealth.in${treatment.attributes?.image?.data?.attributes?.url}`" alt="">
            <h5>{{ treatment.attributes.title }}</h5>
            <p>{{ treatment.attributes.description }}</p>
          </nuxt-link>
        </div>

      </div>

      <div class="text-center">
        <nuxt-link to="/treatment" class="transparentButtonGreen">View More</nuxt-link>
      </div>

    </div>
  </div>

  <div class="container text-center py-5">
    <div class="descriptionSec">
      <h3 class="fw-bold">Orthopedic Services</h3>
      <p class="greyText">
        Our medical team is comprised of some of the finest doctors in the region, renowned for their clinical expertise
        and innovative approaches to medicine.
      </p>
    </div>
  </div>

  <div class="greyBg py-5">
    <div class="container">
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
      <div class="text-center py-5">
        <nuxt-link to="/disease" class="transparentButtonGreen">View More</nuxt-link>
      </div>

    </div>
  </div>

  <div class="container text-center py-5">
    <div class="descriptionSec">
      <h3 class="fw-bold">About Video</h3>
      <p class="greyText">
        Our medical team is comprised of some of the finest doctors in the region, renowned for their clinical expertise
        and innovative approaches to medicine.
      </p>
    </div>
  </div>

  <div class="container">
    <div class="video-player pt-3 pb-5">
      <video class="w-100 plyr-video-player pb-4" playsinline controls>
        <source src="/assets/image/cardiobnrvideo.mp4" type="video/mp4">
      </video>
      <button class="custom-play-button play-button" style="display: none;"><span
          class="material-symbols-outlined custom-play fw-bold">play_arrow</span></button>
    </div>
    <div class="text-end py-3 w-75 mx-auto">
      <span>
        <h4 class="fw-bold d-inline">Dr. Sanmuga sundaram</h4>&emsp;CEO, SS Spine Hospital
      </span>
    </div>
  </div>

  <div class="container my-5">
    <div class="d-flex justify-content-between align-items-center">
      <h3 class="fw-bold">Resources</h3>
      <div>
        <h3 class="fw-bold d-inline mx-sm-3 mx-2">ALL</h3>
        <a href="/blogs"><img src="/assets/image/arrow_circle_right.png" class="arrowImg pb-3" /></a>
      </div>
    </div>
    <div class="row">
      <div class="col-md-4 col-sm-6 col-xs-12 my-3" v-for="blog in blogdata" :key="blog.id">
        <div class="blogcard">
          <nuxt-link :to="`/blogs/${blog.attributes?.slug}`">
            <img v-if="blog.attributes?.blog_card?.image?.data?.attributes?.url" :src="`https://templates.mocerohealth.in${blog.attributes?.blog_card?.image?.data?.attributes?.url}`"
              alt="">
              <div v-else class="dummyimg"></div>
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

let treatment = await useFetch('https://templates.mocerohealth.in/api/treatments?populate=image&pagination[start]=0&pagination[limit]=4');
debugger;
let treatmentdata = treatment.data._rawValue.data
console.log(treatmentdata);

let disease = await useFetch('https://templates.mocerohealth.in/api/diseases?populate=image&pagination[start]=0&pagination[limit]=4');
let diseasedata = disease.data._rawValue.data
console.log(diseasedata);

let blogs = await useFetch('https://templates.mocerohealth.in/api/blogs?populate=blog_card.image&pagination[start]=0&pagination[limit]=3');
debugger
let blogdata = blogs.data._rawValue.data
console.log(blogdata);

onMounted(() => {

  const videoSections = document.querySelectorAll('.video-player');
  videoSections.forEach(section => {


    const video = section.querySelector('.plyr-video-player');
    const playButton = section.querySelector('.play-button');
    let timeoutId;

    function hidePlayButton() {
      playButton.style.display = 'none';
    }

    function showPlayButton() {
      playButton.style.display = 'flex';
    }

    function resetTimeout() {
      clearTimeout(timeoutId);
      timeoutId = setTimeout(hidePlayButton, 2000); // Adjust the timeout duration as needed (3000 milliseconds = 3 seconds)
    }

    playButton.addEventListener('click', function () {
      if (video.paused) {
        video.play();
        playButton.textContent = 'Pause';
      } else {
        video.pause();
        playButton.textContent = 'Play';
      }
      resetTimeout();
    });

    video.addEventListener('play', function () {
      playButton.innerHTML = '<span class="material-symbols-outlined custom-play">pause</span>';
      playButton.style.padding = '10px';
      playButton.style.borderRadius = '50%';
      playButton.style.opacity = '75%';
      resetTimeout();
    });

    video.addEventListener('pause', function () {
      playButton.innerHTML = '<span class="material-symbols-outlined custom-play">play_arrow</span>';
      playButton.style.padding = '10px';
      playButton.style.borderRadius = '50%';
      playButton.style.opacity = '75%';
      resetTimeout();
    });

    video.addEventListener('mousemove', function () {
      showPlayButton();
      resetTimeout();
    });

    video.addEventListener('mouseleave', function () {
      resetTimeout();
    });
    showPlayButton();
    // hidePlayButton();
  });

});
</script>

<style scoped>
.dummyimg{
  width: 100%;
  height: 300px;
  background-color: #e5e5e5;
  border-radius: 10px;
}
</style>