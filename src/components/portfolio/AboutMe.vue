<template>
    <section id="about_me">
        <div class="about-me-main">
            <div>
                <h1>About Me</h1>
            </div>
            <div class="about-me-content">
                <p>I specialize in customizing and configuring Microsoft Dynamics 365 CRM to align with specific business requirements. My expertise includes creating custom entities, fields, forms, and views that enhance user experience and streamline operations.
                I am proficient in client-side scripting using JavaScript, enabling dynamic form behaviors and validations. Additionally, I implement business rules to enforce data integrity and automate processes within the CRM.
                My experience extends to developing and deploying plugins, allowing for the execution of custom business logic during various CRM events. I am also familiar with configuring Dynamics Portals to provide external users with access to CRM data and functionalities.</p>
            </div>
            <div class="skill-images">
                <div v-for="(skill,index) in skillSet" :key="index + 'skill-set'" class="skill-image-class">
                    <div class="skill-image-and-name">
                        <img :src="skill.image" alt="skill-image" style="max-width: 100%;width: 120px;height: 120px;" />
                        <span> {{ skill.name }}</span>
                    </div>
                </div>
            </div>
            
        </div>
    </section>
</template>
<script setup>
    import { ref } from 'vue';
    const skillSet = ref([{
        image: require('@/assets/images/skills/logo1.png'),
        name: 'MS Dynamics 365'
    },
    {
        image: require('@/assets/images/skills/logo2.png'),
        name: 'Power Automate'
    },
    {
        image: require('@/assets/images/skills/logo3.png'),
        name: 'CRM'
    },
    {
        image: require('@/assets/images/skills/logo4.png'),
        name: 'Azure Functions'
    },
    {
        image: require('@/assets/images/skills/logo5.png'),
        name: 'Logic Apps'
    },
    {
        image: require('@/assets/images/skills/logo6.png'),
        name: 'JavaScript'
    },
    {
        image: require('@/assets/images/skills/logo7.png'),
        name: 'C#'
    },
    {
        image: require('@/assets/images/skills/logo8.png'),
        name: 'Visual Studio'
    },
    {
        image: require('@/assets/images/skills/logo9.png'),
        name: 'Postman'
    }]);
</script>
<style>
    @import url(../../assets/styles/AboutMe.scss);
</style>