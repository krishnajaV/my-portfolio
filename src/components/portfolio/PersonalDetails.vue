<template>
    <section id="personal_details">
        <div class="home-page-personal-det">
            <div class="personal_details">
                <h2>Hello <span class="secondary-dot">.</span></h2>
                <div class="personal-name"> <div class="secondary-line"></div> <div>Im {{ name }}</div></div>
                <h1>Software Developer</h1>
                <div class="resume-btn"> <span class="material-symbols-outlined">download</span> <a class="resume-button" href="/assets/resume.pdf" target="_blank" rel="noopener noreferrer">Resume</a> </div>
            </div>
            <div class="personal-photo">
                <div class="circle-photo">
                    <img :src="elipsImage" alt="border-profile-image" style="max-width: 100%; " />
                </div>
                <div  @touchstart="handleTouchStart" @touchend="handleTouchEnd">
                    <span @click.prevent="changeImage('right')" class="material-symbols-outlined left-arrow-btn">keyboard_arrow_left</span>
                    <img :src="profileImage" :class="['profile-image', animationClass]" alt="profile-image" style="max-width: 100%; display: block; position: absolute;" />
                    <span @click.prevent="changeImage('left')" class="material-symbols-outlined right-arrow-btn">keyboard_arrow_right</span>
                </div>
                
            </div>
        </div>
    </section>
</template>
<script setup>
    import { ref } from 'vue'
    const name = ref('Krishnaja')
    const elipsImage = ref(require('@/assets/images/elips.svg'))
    const profileImages = [
        require('@/assets/images/me1.png'),
        require('@/assets/images/me2.png')
    ]
    const currentIndex = ref(0)
    const profileImage = ref(profileImages[currentIndex.value])
    const animationClass = ref('')

    const changeImage = (direction) => {
        animationClass.value = 'fade-out'

        setTimeout(() => {
            if (direction === 'left') {
            currentIndex.value = (currentIndex.value - 1 + profileImages.length) % profileImages.length
            } else if (direction === 'right') {
            currentIndex.value = (currentIndex.value + 1) % profileImages.length
            }

            profileImage.value = profileImages[currentIndex.value]
            animationClass.value = 'fade-in'

            setTimeout(() => {
            animationClass.value = ''
            }, 500) 
        }, 200)
    }
    const touchStartX = ref(0)
    const touchEndX = ref(0)
    const handleTouchStart = (e) => {
        touchStartX.value = e.changedTouches[0].screenX
    }
    const handleTouchEnd = (e) => {
        touchEndX.value = e.changedTouches[0].screenX
        handleSwipe()
    }
    const handleSwipe = () => {
    const diff = touchStartX.value - touchEndX.value
    if (Math.abs(diff) > 50) {
        if (diff > 0) {
        changeImage('right') 
        } else {
        changeImage('left')
        }
    }
    }
</script>
<style>
    @import url(../../assets/styles/PersonalDetails.scss);
</style>