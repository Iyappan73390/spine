<template>
  <Header />
<div class="container">
    <div class="row">
        <div class="col-md-12 bnr">
          <img src="/assets/image/line.png" class="line1" alt="">
            <h1><span>Patient Stories</span></h1>
            <h1>We help our patients heal</h1>
          <img src="/assets/image/line.png" class="line2" alt="">
        </div>
    </div>
</div>
<div class="carousel-wrapper">
    <div class="carousel">
        <div class="item"><img src="/assets/image/pat1.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat2.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat3.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat1.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat2.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat3.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat1.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat2.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat3.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat1.png" alt="patient"></div>
        <!-- DUPLICATE -->
        <div class="item"><img src="/assets/image/pat2.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat3.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat1.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat2.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat3.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat1.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat2.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat3.png" alt="patient"></div>
        <div class="item"><img src="/assets/image/pat1.png" alt="patient"></div>
    </div>
</div>

<section class="extensivecare">
    <div class="container">
        <h4 class="mb-5 "><b>We help our patients with extensive care</b></h4>

        <div class="row">
            <div class="col-md-4 col-sm-6 col-xs-12 mb-3">
                <div class="icondiv">
                    <img src="/assets/image/extensive1.png" alt="">
                </div>
                <p class="mb-2"><b>Patient service</b></p>
                <p>You'll have a branded job board as a centralized place to display all the open positions at your organization.</p>
            </div>
            <div class="col-md-4 col-sm-6 col-xs-12 mb-3">
                <div class="icondiv">
                    <img src="/assets/image/extensive2.png" alt="">
                </div>
                <p class="mb-2"><b>Patient Care</b></p>
                <p>You'll have a branded job board as a centralized place to display all the open positions at your organization.</p>
            </div>
            <div class="col-md-4 col-sm-6 col-xs-12 mb-3">
                <div class="icondiv">
                    <img src="/assets/image/extensive3.png" alt="">
                </div>
                <p class="mb-2"><b>Happy Patient</b></p>
                <p>You'll have a branded job board as a centralized place to display all the open positions at your organization.</p>
            </div>
        </div>
    </div>
</section>

      <div class="container py-5">
          <nav class="d-flex justify-content-center">
              <div class="nav nav-tabs reviewTab" id="nav-tab" role="tablist">
                  <button class="nav-link active" id="googleReview" data-bs-toggle="tab"
                    data-bs-target="#nav-googleReview" type="button"
                    role="tab" aria-controls="nav-googleReview"
                    aria-selected="true">
                    Google Review
                  </button>
                  <button class="nav-link" id="googleReview" data-bs-toggle="tab"
                    data-bs-target="#nav-videoTestimonials" type="button"
                    role="tab" aria-controls="nav-videoTestimonials"
                    aria-selected="true">
                    Video Testimonials
                  </button>
              </div>
          </nav>

          <div class="tab-content video-tab my-5" id="nav-tabContent">
            <div class="tab-pane fade show active" id="nav-googleReview" role="tabpanel" aria-labelledby="nav-videoTestimonials-tab'">
                <div class="testimonialcard">
                  <img src="/assets/image/leaf.png" class="img-fluid leaf" alt="">
                  <p>Knowledgeable, caring, kind and friendly doctor. Friendly and service oriented staff. I would highly recommend the doctor for all your ortho needs. 
                    He instilled great confidence in me for my speedy recovery. Thanks to him and his staff.Knowledgeable, caring, kind and friendly doctor. Friendly 
                    and service oriented staff. I would highly recommend the doctor for all your ortho needs. He instilled great confidence in me for my speedy recovery. 
                    Thanks to him and his staff.</p>

                      <div class="reviewsec">
                        <img src="/assets/image/review.png" class="img-fluid review" alt="">
                        <div class="stardiv">
                          <p>Esther Jackson</p>
                          <img src="/assets/image/star.png" class="img-fluid" alt="">
                        </div>
                      </div>
                </div>
            </div>
            <div class="tab-pane fade" id="nav-videoTestimonials" role="tabpanel" aria-labelledby="nav-videoTestimonials-tab'">
              <div class="testimonialcard">
                  <p>SOON</p>
                </div>
            </div>
          </div>
      </div>

    <div class="container my-5">
        <div class="row">
            <div class="happypat">
                <img src="/assets/image/happypat.png" class="img-fluid mb-4 mt-5" alt="">
                <h3 class="mb-3">10,000 Happy patients visit my hospital</h3>
                <p>Visited lot of places for backpain for 6months not recover.. visited Dr.p.shanmuga sundharam he explained very well..now after surgery Doing well</p>
                <div class="write">
                  <h4>Write Your Feedback</h4>
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
</script>

<style scoped>
.extensivecare{
  padding: 100px 0px;
  background: rgb(202,231,235);
  background: linear-gradient(103deg, rgba(202,231,235,1) 0%, rgba(202,231,235,1) 0%, rgba(193,210,255,1) 87%);
}
.extensivecare h4{
  color: #000000;
}
.icondiv{
  width: 40px;
  height: 40px;
  border-radius: 5px;
  background-color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px;
}
.line1{
    position: absolute;
    top: 44%;
    z-index: -1;
}
.line2{
    position: absolute;
    top: 57%;
    z-index: -1;
}
.bnr{
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  width: 100%;
  height: 50vh;
}
.bnr h1{
  font-size: 55px;
  color: #444444;
  font-weight: 500;
}
.bnrtxt{
    color: #444444;
    text-align: center;
}

.testimonialcard{
  background: #164A87;
  padding: 60px 30px;
  border-radius: 15px;
  position: relative;
  width: 70%;
  margin: auto;
  line-height: 2;
}
.testimonialcard .leaf{
    position: absolute;
    bottom: 0;
    right: 0;
    width: 70%;
    height: 100%;
}
.testimonialcard p{
  color: #fff;
}
.reviewsec{
  display: flex;
  align-items: center;
  line-height: 1.5;
}
.reviewsec .review{
  width: 60px;
  height: 60px;
  margin-right: 10px;
}
.stardiv p{
  margin-bottom: 0;
}
.stardiv img{
  width: 100px;
}
.reviewsec:before,
.reviewsec:after {
	position: absolute;
	color: #2b5b93;
}
.reviewsec:after {
	content: '”';
	right: 18%;
	top: 14%;
  font-size: 27rem;
}




.happypat{
    background-color: #FDF4E6;
    padding: 50px 30px;
    text-align: center;
    width: 70%;
    margin: auto;
    border-radius: 10px;
}
.happypat h3{
  font-weight: 700;
  font-size: 40px;
  color: #190041;
}
.happypat p{
  color: #190041;
  font-size: 16px;
  font-weight: 500;
}
.happypat .write{
  background: #fff;
  padding: 15px 50px;
  display: inline-block;
  border-radius: 30px;
}
.happypat .write h4{
  font-weight: 700;
  color: #164A87;
  margin-bottom: 0;
}
.carousel-wrapper {
  --width: 450px;
  --gap: 0;
  --num-items: 10;
  --ani-offset: calc(var(--width) * var(--num-items) * -1);
  --ani-speed: 20s;
  
  width: 100%;
  overflow: hidden;
  position: relative;
}
.carousel-wrapper::before,
.carousel-wrapper::after{
  content: '';
  position: absolute;
  /* width: 20%; */
  height: 100%;
  z-index: 1;
  top: 0;
}
.carousel-wrapper::before{
  left: 0;
  background-image: linear-gradient(to right,var(--bg-clr) 0%,transparent 50%);
}
.carousel-wrapper::after{
  right: 0;
  background-image: linear-gradient(to left,var(--bg-clr) 0%,transparent 50%);
}

.carousel {
  display: flex;
  align-items: center;
  animation: slide var(--ani-speed) linear infinite;
}
.item{
  flex: 1 0 var(--width);
  text-align: center;
  padding:1rem;
}
.item > img{
  width: 100%;
  height: auto;
  object-fit: cover;
}

@keyframes slide {
  100% {
    transform: translateX(var(--ani-offset));
  }
}
@media only screen and (max-width: 768px) {
  .reviewsec:before,
.reviewsec:after {
	display: none;
}
.testimonialcard .leaf{
  display: none;
}
  .bnr h1{
    font-size: 44px;
    color: #444444;
    font-weight: 500;
  }
  .line1{
    position: absolute;
    top: 44%;
    z-index: -1;
    width: 60%;
  }
  .line2{
    position: absolute;
    top: 55%;
    z-index: -1;
    width: 90%;
  }
  .happypat{
    width: 100%;
  }
  .testimonialcard{
    width: 100%;
  }
}
@media only screen and (max-width: 568px) {
  .bnr h1{
    font-size: 28px;
    color: #444444;
    font-weight: 500;
  }
  .line1{
    position: absolute;
    top: 44%;
    z-index: -1;
    width: 60%;
  }
  .line2{
    position: absolute;
    top: 55%;
    z-index: -1;
    width: 90%;
  }
}

</style>