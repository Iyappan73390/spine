<template>
    <Header />
    <div class="booksec">
        <div class="container">
            <div class="row">
                <h3>Book an Appointment</h3>
                <p>Easily schedule your visit with our expert specialist by filling this form.</p>
            </div>
        </div>
    </div>

    <div class="my-3">
        <ul class="nav nav-pills justify-content-center" role="tablist">
            <li class="nav-item" role="presentation"><a class="nav-link active" data-bs-toggle="pill" href="#ssortho"
                    aria-selected="true" role="tab">SS Ortho</a></li>
            <li class="nav-item" role="presentation"><a class="nav-link" data-bs-toggle="pill" href="#medway"
                    aria-selected="false" role="tab" tabindex="-1">Medway Hospital</a></li>
        </ul>
    </div>

    <div class="tab-content press-room-tab-content">
        <div id="ssortho" class="container tab-pane active show" role="tabpanel">
            <div class="container">
                <div class="row forms">
                    <div class="col-md-12 col-sm-12 mb-3">
                        <label class="form-label">Patient Full Name</label>
                        <input type="text" class="form-control" v-model="formData.fullname" />
                        <span id="errfullname" class="text-danger">{{ errors.fullname }}</span>
                    </div>
                    <div class="col-md-6 col-sm-12 mb-3">
                        <label class="form-label">Date of Birth</label>
                        <input type="date" class="form-control" v-model="formData.dob" />
                        <span id="errdob" class="text-danger">{{ errors.dob }}</span>
                    </div>
                    <div class="col-md-6 col-sm-12 mb-3">
                        <label class="form-label">Gender</label>
                        <div class="gendercol">
                            <div>
                                <input type="radio" value="Male" v-model="formData.gender" />
                                <label for="">Male</label>
                            </div>
                            <div>
                                <input type="radio" value="Female" v-model="formData.gender" />
                                <label for="">Female</label>
                            </div>
                            <div>
                                <input type="radio" value="Do not Want to disclose" v-model="formData.gender" />
                                <label for="">Do not Want to disclose</label>
                            </div>
                        </div>
                        <span id="errgender" class="text-danger">{{ errors.gender }}</span>
                    </div>
                    <div class="col-md-12 col-sm-12 mb-3">
                        <label class="form-label">Aadhar Number (Not Mandatory)</label><br>
                        <small>By providing Aadhar will help us to pre-validate your data</small>
                        <input type="text" class="form-control" v-model="formData.aadhar" />
                        <span id="erraadhar" class="text-danger">{{ errors.aadhar }}</span>
                    </div>
                    <div class="col-md-12 col-sm-12 mb-3">
                        <label class="form-label">Email</label>
                        <input type="email" class="form-control" v-model="formData.email" />
                        <span id="erremail" class="text-danger">{{ errors.email }}</span>
                    </div>
                    <div class="col-md-6 col-sm-12 mb-3">
                        <label class="form-label">Mobile</label>
                        <input type="tel" class="form-control" v-model="formData.mobile" />
                        <span id="errmobile" class="text-danger">{{ errors.mobile }}</span>
                    </div>
                    <div class="col-md-6 col-sm-12 mb-3">
                        <label class="form-label">Alternative Number</label>
                        <input type="tel" class="form-control" v-model="formData.altno" />
                        <span id="erraltno" class="text-danger">{{ errors.altno }}</span>
                    </div>
                    <div class="col-md-12 col-sm-12 mb-3">
                        <label class="form-label">Address</label>
                        <textarea class="form-control" cols="30" rows="5" v-model="formData.address"></textarea>
                        <span id="erraddress" class="text-danger">{{ errors.address }}</span>
                    </div>
                    <div class="text-center my-3">
                        <button class="btn submit" @click="submitForm">Submit</button>
                    </div>
                </div>
            </div>
        </div>
        <div id="medway" class="container tab-pane fade" role="tabpanel">
            <div class="container">
                <div class="row forms">
                    <div class="col-md-12 col-sm-12 mb-3">
                        <label class="form-label">Patient Full Name</label>
                        <input type="text" class="form-control" v-model="formData.fullname" />
                        <span id="errfullname" class="text-danger">{{ errors.fullname }}</span>
                    </div>
                    <div class="col-md-6 col-sm-12 mb-3">
                        <label class="form-label">Date of Birth</label>
                        <input type="date" class="form-control" v-model="formData.dob" />
                        <span id="errdob" class="text-danger">{{ errors.dob }}</span>
                    </div>
                    <div class="col-md-6 col-sm-12 mb-3">
                        <label class="form-label">Gender</label>
                        <div class="gendercol">
                            <div>
                                <input type="radio" value="Male" v-model="formData.gender" />
                                <label for="">Male</label>
                            </div>
                            <div>
                                <input type="radio" value="Female" v-model="formData.gender" />
                                <label for="">Female</label>
                            </div>
                            <div>
                                <input type="radio" value="Do not Want to disclose" v-model="formData.gender" />
                                <label for="">Do not Want to disclose</label>
                            </div>
                        </div>
                        <span id="errgender" class="text-danger">{{ errors.gender }}</span>
                    </div>
                    <div class="col-md-12 col-sm-12 mb-3">
                        <label class="form-label">Aadhar Number (Not Mandatory)</label><br>
                        <small>By providing Aadhar will help us to pre-validate your data</small>
                        <input type="text" class="form-control" v-model="formData.aadhar" />
                        <span id="erraadhar" class="text-danger">{{ errors.aadhar }}</span>
                    </div>
                    <div class="col-md-12 col-sm-12 mb-3">
                        <label class="form-label">Email</label>
                        <input type="email" class="form-control" v-model="formData.email" />
                        <span id="erremail" class="text-danger">{{ errors.email }}</span>
                    </div>
                    <div class="col-md-6 col-sm-12 mb-3">
                        <label class="form-label">Mobile</label>
                        <input type="tel" class="form-control" v-model="formData.mobile" />
                        <span id="errmobile" class="text-danger">{{ errors.mobile }}</span>
                    </div>
                    <div class="col-md-6 col-sm-12 mb-3">
                        <label class="form-label">Alternative Number</label>
                        <input type="tel" class="form-control" v-model="formData.altno" />
                        <span id="erraltno" class="text-danger">{{ errors.altno }}</span>
                    </div>
                    <div class="col-md-12 col-sm-12 mb-3">
                        <label class="form-label">Address</label>
                        <textarea class="form-control" cols="30" rows="5" v-model="formData.address"></textarea>
                        <span id="erraddress" class="text-danger">{{ errors.address }}</span>
                    </div>
                    <div class="text-center my-3">
                        <button class="btn submit" @click="submitForm">Submit</button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <section class="subscribesec">
        <div class="container">
            <div class="row">
                <h3>Subscribe to the News letter of the Hospital</h3>
                <p>Receive the latest news and happening from our institution directly to your email</p>
            </div>
            <div class="row">
                <div class="col-md-4 col-sm-12 mb-3">
                    <input type="text" class="form-control" placeholder="Full Name">
                </div>
                <div class="col-md-4 col-sm-12 mb-3">
                    <input type="text" class="form-control" placeholder="Email" />
                </div>
                <div class="col-md-4 col-sm-12 mb-3">
                    <button class="subscribe">Subscribe</button>
                </div>
            </div>
        </div>
    </section>

    <Footer />
</template>

<script setup>
import { reactive } from 'vue'

useHead({
  title: 'SS Spine & Ortho Clinic'
})

const formData = reactive({
    fullname: '',
    dob: '',
    gender: '',
    aadhar: '',
    email: '',
    mobile: '',
    altno: '',
    address: ''
})

const errors = reactive({
    fullname: '',
    dob: '',
    gender: '',
    aadhar: '',
    email: '',
    mobile: '',
    altno: '',
    address: ''
})

const validateForm = () => {
    let isValid = true

    // Clear previous errors
    for (const key in errors) {
        errors[key] = ''
    }

    // Validate fullname
    if (!formData.fullname) {
        errors.fullname = 'Full name is required'
        isValid = false
    }

    // Validate dob
    if (!formData.dob) {
        errors.dob = 'Date of birth is required'
        isValid = false
    }

    // Validate gender
    if (!formData.gender) {
        errors.gender = 'Gender is required'
        isValid = false
    }

    // Validate email
    const emailPattern = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/
    if (!formData.email) {
        errors.email = 'Email is required'
        isValid = false
    } else if (!emailPattern.test(formData.email)) {
        errors.email = 'Invalid email address'
        isValid = false
    }

    // Validate mobile
    const mobilePattern = /^[0-9]{10}$/
    if (!formData.mobile) {
        errors.mobile = 'Mobile number is required'
        isValid = false
    } else if (!mobilePattern.test(formData.mobile)) {
        errors.mobile = 'Invalid mobile number'
        isValid = false
    }

    // Validate altno (optional, but if provided should be valid)
    if (formData.altno && !mobilePattern.test(formData.altno)) {
        errors.altno = 'Invalid alternative number'
        isValid = false
    }

    // Validate address
    if (!formData.address) {
        errors.address = 'Address is required'
        isValid = false
    }

    return isValid
}

const submitForm = async () => {
    if (validateForm()) {
        console.log('Form Data:', formData)

        const bname = `Hi <br/> Name : ${formData.fullname} <br/> Date of Birth : ${formData.dob} <br/> Gender : ${formData.gender} <br/> Aadhar Number : ${formData.aadhar} <br/> Email : ${formData.email} <br/> Phone Number : ${formData.mobile} <br/> Alternative Number : ${formData.altno} <br/> Address : ${formData.address}`

        const FORMDataContact = {
            from_emailid: "ssspinedigital@gmail.com",
            password: "lweezobxgftmfivj",
            to_emailid: "iyyappan@mocerohealth.in",
            cc_emailid: "iyyappan@mocerohealth.in",
            email_subject: "Website Query",
            fields0: bname,
            fields1: null,
            fields2: null,
            fields3: null,
            fields4: null,
            fields5: null,
            fields6: null,
            fields7: null,
            fields8: null,
            fields9: null,
            fields10: null,
            Attachmentfilename: ""
        }

        try {
            const response = await fetch('https://hms-devapi.mocerohealth.in/api/WebSiteEmail/WebSiteEmail_Send', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify(FORMDataContact)
            })

            const data = await response.json()
            if (data.status) {
                alert("Mail Sent Successfully")

                // Clear form fields
                formData.fullname = ''
                formData.dob = ''
                formData.gender = ''
                formData.aadhar = ''
                formData.email = ''
                formData.mobile = ''
                formData.altno = ''
                formData.address = ''
            } else {
                alert("Failed to send mail")
            }
        } catch (error) {
            console.error("Error sending mail:", error)
            alert("Error sending mail")
        }
    }
}
</script>

<style scoped>
.subscribesec{
    background-color: #F3F3F3;
    padding: 50px 0px;
    margin-top: 50px;
}
.subscribesec h3{
    font-weight: 500;
}
.subscribesec p{
    font-size: 14px;
    margin-bottom: 30px;
}
.subscribesec input{
    border-radius: 30px;
    outline: none;
    border: none;
    padding: 10px
}
.subscribesec button{
    background-color: #0C8CE9;
    border-radius: 30px;
    outline: none;
    border: none;
    color: #ffffff;
    padding: 10px;
}
.booksec {
    background: #F7F7F7;
    padding: 70px 0;
}

.booksec h3 {
    font-weight: 700;
    color: #444444;
}

.booksec p {
    color: #444444;
}

.nav-pills .nav-link.active {
    background-color: #233B77;
    color: #ffffff;
    border-radius: 30px;
}

.nav-pills .nav-link {
    background-color: #F7F7F7;
    color: #444444;
    border-radius: 30px;
    margin: 0 10px;
}

.forms label {
    color: #444444;
    font-size: 16px;
}

.forms input {
    border: 1px solid #E1E1E1 !important;
}

.gendercol {
    background-color: #FAFBFE;
    padding: 10px;
    width: 70%;
    display: flex;
}

.gendercol input {
    margin: 0 10px;
}

.gendercol div {
    margin: 0 10px;
}

.submit {
    background-color: #0C8CE9;
    padding: 10px 140px;
    border-radius: 30px;
    color: #ffffff;
}

@media only screen and (max-width: 868px) {
    .gendercol {
        width: 100%;
    }

    .gendercol label {
        font-size: 14px;
    }

    .gendercol input {
        margin: 7px;
    }

    .gendercol div {
        margin: 0;
    }
}
</style>