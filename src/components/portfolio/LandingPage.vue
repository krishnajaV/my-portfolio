<template>
    <div>
        <div v-if="isLoading" class="landing-page">
            <div class="initial-logo">
                <span class="logo-letter">KJ</span>
            </div>
        </div>
        <div class="" v-else>
            <HeaderComponent></HeaderComponent>
            <MainPage></MainPage>
        </div>
    </div>
</template>
<script setup>
    import MainPage from "./MainPage.vue"
    import HeaderComponent from "./HeaderComponent.vue"
    import {ref,onMounted} from "vue"
    const isLoading = ref(true) 
    onMounted(()=>{
        setTimeout(()=>{
            isLoading.value = false;
        },500)
    })
</script>
<style>
    @import url('../../assets/styles/landingPage.scss');
</style>