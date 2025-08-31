<template>
    <div>
        <header class="header">
            <nav class="nav-bar-class">
                <h6 @click="scrollToSection('personal_details')" class="full-name"> Krishnaja V</h6>
                <div @click="scrollToSection('personal_details')" class="front-page-logo"><span class="front-page-logo-letter">KJ</span></div>
                <div class="burger-menu" v-if="!isShowMenuForMobile" @click="activeMenuToggle"><span class="material-symbols-outlined">menu</span></div>
                <div class="burger-menu" v-else @click="closeTogleMenu"><span class="material-symbols-outlined">close</span></div>
                <div class="nav-items" :class="{active : isShowMenuForMobile}">
                    <ol>
                        <li><a @click.prevent="scrollToSection('personal_details')">Home</a></li>
                        <li><a @click.prevent="scrollToSection('about_me')">About</a></li>
                        <li><a @click.prevent="scrollToSection('experience')">Experience</a></li>
                        <li><a @click.prevent="scrollToSection('contact_me')">Contact</a></li>
                    </ol>
                </div>
            </nav>
        </header>
    </div>

</template>
<script setup>
import {ref} from 'vue'
const isShowMenuForMobile = ref(false);
const activeMenuToggle = () =>{
    isShowMenuForMobile.value = true;
}
const closeTogleMenu = () =>{
    isShowMenuForMobile.value = false;
}
const scrollToSection = (sectionId) =>{
    const element = document.getElementById(sectionId);
    if(element){
        window.scrollTo({
            top:element.offsetTop -100,
            behavior:'smooth'
        })
        isShowMenuForMobile.value = false;
    }
}
</script>

<style>
    @import url(../../assets/styles/Header.scss);
   
</style>