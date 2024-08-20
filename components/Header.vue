<template>
    <div>
        <div class="navbar navbar-expand-lg navPos" id="pcNavbar">
            <div class="container navSec">
                <a class="navbar-brand p-0" href="/">
                    <img src="/assets/image/SSspineLogo.png" class="headerLogo" />
                </a>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                    data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent"
                    aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <!-- pc menu start -->
                <div class="collapse navbar-collapse">
                    <ul class="navbar-nav mb-0 navbar-wrap py-3">
                        <li class="nav-item">
                            <a href="/" class="nav-link" aria-current="page">
                                Home
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="/doctor" class="nav-link" aria-current="page">
                                About Doctor
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="/disease" class="nav-link" aria-current="page">
                                Conditions
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="/treatment" class="nav-link" aria-current="page">
                                Treatments
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="/blogs" class="nav-link" aria-current="page">
                                Blogs
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="/testimonial" class="nav-link" aria-current="page">
                                Patient Story
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="/contact-us" class="nav-link" aria-current="page">
                                Contact Us
                            </a>
                        </li>
                        <div>
                            <a href="/book-an-appointment" class="nav-link btn menuButton" @click="menuItem.action">
                                Book an Appointment
                            </a>
                        </div>
                    </ul>
                </div>
            </div>
        </div>
        <nav class="mobile-nav" id="mobileNavbar">
            <div class="mobileNavOverlay" :class="{ 'active': isMenuOpen }" @click="closeMenu"></div>
            <ul class="navUl pt-4" :class="{ 'slider': isMenuOpen }">
                <li class="px-4">
                    <a href="#"><img src="" class="" /></a>
                </li>
                <li class="nav-item">
                            <a href="/" class="nav-link" aria-current="page">
                                Home
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="/doctor" class="nav-link" aria-current="page">
                                About Doctor
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="/disease" class="nav-link" aria-current="page">
                                Conditions
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="/treatment" class="nav-link" aria-current="page">
                                Treatments
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="/blogs" class="nav-link" aria-current="page">
                                Blogs
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="/testimonial" class="nav-link" aria-current="page">
                                Patient Story
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="/contact-us" class="nav-link" aria-current="page">
                                Contact Us
                            </a>
                        </li>
                        <li class="nav-item">
                            <a href="/" class="nav-link btn menuButton color-changing-button" @click="menuItem.action">Book an Appointment</a>
                        </li>
            </ul>
            <div class="d-flex align-items-center justify-content-between py-2">
                <div class="burger" @click="toggleMenu">
                    <span class="line"></span>
                    <span class="line"></span>
                    <span class="line"></span>
                </div>
                
                <div class="headerMblLogoSec">
                    <a class="navbar-brand headerMblLogo p-0" href="/"><img src="/assets/image/SSspineLogo.png" class="" /></a>
                </div>
            </div>
        </nav>
    </div>
</template>
  
<script setup>
    // const headerRaw = await useFetch('https://templates.mocerohealth.in/api/main-menu?populate[0]=MainMenuItem&populate[1]=MainMenuItem.headers&populate[2]=MainMenuItems.headers.dropdown_links');
    // let headerData = headerRaw.data._rawValue.data;
    // console.log('headerData', headerData);
    // let mainMenuData = headerData?.attributes?.MainMenuItems;

    const isMenuOpen = ref(false);

    const toggleMenu = () => {
        isMenuOpen.value = !isMenuOpen.value;
    };

    const closeMenu = () => {
        isMenuOpen.value = false;
    };

    const handleClickOutside = (event) => {
        const navUl = document.querySelector('.navUl');
        const burger = document.querySelector('.burger');
        if (navUl && !navUl.contains(event.target) && !burger.contains(event.target)) {
            closeMenu();
        }
    };

    onMounted(() => {
        document.addEventListener('click', handleClickOutside);
    });

    onUnmounted(() => {
        document.removeEventListener('click', handleClickOutside);
    });
</script>
  