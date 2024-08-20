<template>
    <Header />
    <section class="contactussec">
        <img src="/assets/image/contactus.png" alt="">
    </section>
    <div class="container my-5">
        <div class="row">
            <div class="col-lg-6 col-md-6 col-sm-12">
                <h4>SS Spine & Ortho Clinic</h4>
                <div class="row contactdetails align-items-center">
                    <div class="col-md-4">
                        <p><b>Email</b></p>
                        <p><b>Phone Number</b></p>
                        <p class="mb-5"><b>Address</b></p>
                        <p><b>Directions (Transport)</b></p>
                    </div>
                    <div class="col-md-8">
                        <p><a href="mailto: ssspinedigital@gmail.com">ssspinedigital@gmail.com</a></p>
                        <p><a href="tel: 97909 77646">97909 77646</a></p>
                        <p>No-42, Valaiyapathi Salai, Block 2, J J Nagar, Mogappair East, Chennai-37</p>
                        <p>Central Railway Station (via Beach Road): 30 minutes with traffic.
                            Koyambedu Bus Terminus: 60 minutes with traffic.</p>
                    </div>
                </div>
            </div>
            <div class="col-lg-6 col-md-6 col-sm-12">
                <iframe
                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3886.2837943433906!2d80.18540017575674!3d13.081192012464657!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3a5264007a118a0b%3A0xc9782977f54f05e9!2s42%2C%20Valaiyapathi%20Salai%2C%20Block%205%2C%20Mogappair%2C%20Chennai%2C%20Tamil%20Nadu%20600050!5e0!3m2!1sen!2sin!4v1719830126957!5m2!1sen!2sin"
                    width="600" height="450" style="border:0;" loading="lazy"
                    referrerpolicy="no-referrer-when-downgrade"></iframe>
            </div>
        </div>

        <div class="formdiv my-5">
            <div class="row text-center my-4">
                <h4>Got Questions? We've Got Answers!</h4>
                <p>Use the form below to send us a message and we'll be happy to assist you.</p>
            </div>
            <div class="row">
                <div class="col-sm-6 col-xs-12 mb-3">
                    <label class="form-label">FIRST NAME</label>
                    <input type="email" class="form-control" id="email">
                    <span id="errfirstname"></span>
                </div>
                <div class="col-sm-6 col-xs-12 mb-3">
                    <label class="form-label">LAST NAME</label>
                    <input type="email" class="form-control" id="email">
                    <span id="errlastname"></span>
                </div>
                <div class="col-sm-6 col-xs-12 mb-3">
                    <label class="form-label">PHONE NUMBER</label>
                    <input type="email" class="form-control" id="email">
                    <span id="errphoneno"></span>
                </div>
                <div class="col-sm-6 col-xs-12 mb-3">
                    <label class="form-label">EMAIL ID</label>
                    <input type="email" class="form-control" id="email">
                    <span id="erremail"></span>
                </div>
                <div class="col-sm-12 col-xs-12 mb-3">
                    <label class="form-label">QUERIES/COMMENTS/FEEDBACK</label>
                    <textarea class="form-control" name="" id="" cols="30" rows="6"></textarea>
                </div>
                <div class="text-center">
                    <button class="btn submit" id="submit">Submit</button>
                </div>
            </div>
        </div>


        <div class="builtsec">
            <h3>Built for teams of
                today, like yours.</h3>
            <div class="searchbox-wrap">
                <input type="text" placeholder="Search for something...">
                <button><span>Send</span></button>
            </div>
            <p>Zero commitments - get started for free</p>
            <img src="/assets/image/builtteam.png" class="builtimg" alt="">
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
.contactussec{
    background-color: #164A87;
    padding: 30px;
}
.contactussec img{
    width: 70%;
    display: block;
    margin-left: auto;
    margin-right: auto;
}
h4 {
    font-weight: 600;
    margin-bottom: 20px;
}

.contactdetails {
    color: #999999;
}

.contactdetails p {
    margin-bottom: 40px;
}

.contactdetails p b {
    color: #444444;
}

.contactdetails a {
    text-decoration: none;
    color: #999999;
}

iframe {
    width: 100%;
    height: 400px;
    border-radius: 20px;
}

.formdiv {
    box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 5px 0px, rgba(0, 0, 0, 0.1) 0px 0px 1px 0px;
    padding: 40px;
    border-radius: 10px;
}
.formdiv label{
    color: #999999;
}
.submit{
    background: #0C8CE9;
    padding: 10px 60px;
    border-radius: 40px;
    color: #fff;
    outline: none;
    border: none;
    margin-top: 30px;
}
.submit:focus{
    border: 1px solid #0C8CE9;
}
.builtsec{
    background-color: #292929;
    padding: 50px;
    color: #fff;
    position: relative;
    height: 450px;
    margin-top: 150px;
}
.builtimg{
    position: absolute;
    right: -6%;
    top: -24%;
    width: 45%;
}

.searchbox-wrap {
	 display: flex;
	 width: 500px;
     margin: 10px 0;
}
 .searchbox-wrap input {
	 flex: 1;
	 padding: 10px;
	 font-size: 1.1em;
     outline: none;
	 box-shadow: none;
	 border: none;
     background: transparent;
     border: 1px solid #fff;
     border-right: 0px solid #fff;
}
 .searchbox-wrap button {
	 padding: 10px;
     background-color: #fff;
	 box-shadow: 5px 4px 6px rgba(0,0,0,0.19);
	 border: none;
	 cursor: pointer;
	 cursor: hand;
     border-top: 1px solid #fff;
     border-bottom: 1px solid #fff;
     border-right: 1px solid #fff;
     outline: none;
}
 .searchbox-wrap button span {
	 font-size: 0.9em;
	 text-transform: uppercase;
	 font-weight: 300;
	 color: #292929;
	 border-radius: 20px;
}
@media only screen and (max-width: 868px) {
    .builtsec{
        padding: 35px;
    }
    .searchbox-wrap{
        width: 100%;
    }
    .builtsec{
        height: 320px;
    }
    .builtimg{
        position: absolute;
        right: 1%;
        top: 60%;
        width: 38%;
    }
}
@media only screen and (max-width: 568px) {
    .builtsec{
        padding: 35px;
    }
    .searchbox-wrap{
        width: 100%;
    }
    .builtsec{
        height: 320px;
    }
    .builtimg{
        position: absolute;
        right: 1%;
        top: 66%;
        width: 58%;
    }
}
</style>