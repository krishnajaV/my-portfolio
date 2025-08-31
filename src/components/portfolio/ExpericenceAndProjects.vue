<template>
    <section class="experience-project" id="experience">
        <div class="experience-project-sub">
            <h1> Experience & Project</h1>
        </div>
        <div class="experience-section">
            <div class="section-headings"><span class="material-symbols-outlined">work</span> Experience</div>
            <div v-for="(experience,index) in experiences" :key="'experience-details' + index">
                <h1><span class="material-symbols-outlined">work</span> <span class="secondary-color-name"> {{ experience.name }}</span></h1>
                <div class="experience-details">
                    <div class="employer-details">Employer : <span class="secondary-color-name">{{ experience.employer }}</span></div>
                    <div class="duration"> <span class="material-symbols-outlined">calendar_month</span> &nbsp;{{ experience.startDate}} - {{ experience.endDate}}  </div> 
                    <div class="location"> <span class="material-symbols-outlined">near_me</span> &nbsp;{{ experience.location}} </div> 
                </div>
                <div> 
                    <p class="experience-descriptions">{{ experience.description }}</p>
                </div>
            </div>
        </div>
        <div class="project-section">
            <div class="section-headings"><span class="material-symbols-outlined">assignment</span> Projects</div>
            <div v-for="(project,index) in projects" :key="'project-details' + index">
                <h1><span class="material-symbols-outlined">assignment</span> <span class="secondary-color-name">{{ project.name }}</span></h1>
                <div class="clint-and-skills">
                    <div class="client-details">Client : <span class="secondary-color-name">{{ project.client }}</span></div>
                    <template v-for="(skill,index) in project.skills" :key="'project-skills' + index">
                        <div class="project-skill-set"> {{ skill }}</div> 
                    </template>
                </div>
                <div> 
                    <p class="project-descriptions">{{ project.description }}</p>
                </div>
            </div>
        </div>
        <div class="award-section">
            <div class="section-headings"><span class="material-symbols-outlined">social_leaderboard</span> Awards</div>
            <div> 
                <p class="award-lists">PL-900: Microsoft Power Platform Fundamentals</p>
                <p class="award-lists">AI 100 : Microsoft azure AI Fundamental</p>
                <p class="award-lists">PL 400: Microsoft Power Platform Developer</p>
            </div>
        </div>
    </section>
</template>
<script setup>
    import {ref} from 'vue'
    const projects = new ref([{
        "name":"WWLPBD",
        "client":"Microsoft",
        "description":"The WWLPBD project for Microsoft involved working extensively with Microsoft Dynamics 365 CRM, focusing on system customization and configuration to align with client requirements. The role included implementing client-side scripting and business rules using JavaScript, along with basic customization through the Dynamics Portal. Responsibilities also involved plugin registration and deployment within the CRM environment. Additionally, the project offered exposure to workflow automation using tools such as Azure Functions, Logic Apps, and Power Automate.",
        "skills":["Dynamics 365","CRM","JavaScript","Dynamics Portal"]
    },
    {
        "name":"CDOT",
        "client":"Microsoft",
        "description":"The CDOT project for Microsoft focused on tailoring Microsoft Dynamics 365 to meet complex business requirements through advanced customization. This involved creating and configuring custom entities, relationships, and fields to enhance data management. JavaScript was used extensively for form scripting, enabling real-time validation and dynamic behaviors to improve user experience and data accuracy. Additionally, complex Business Process Flows were designed across multiple entities to streamline and automate end-to-end business operations.",
        "skills":["Dynamics 365","JavaScript","Dynamics Portal"]
    },
    {
        "name":"Strategic Ventures Team Apps",
        "client":"Microsoft",
        "description":"The Strategic Ventures Team Apps project for Microsoft involved enhancing Dynamics 365 solutions with a strong focus on security, performance, and user adoption. Key responsibilities included implementing field-level security to safeguard sensitive data, optimizing client-side performance through efficient JavaScript practices, and delivering end-user training and support to ensure smooth adoption of system enhancements.",
        "skills":["Dynamics 365","JavaScript","Dynamics Portal"]
    }])
    const experiences = new ref([{
        "name":"System Engineer",
        "employer":"Infosys Limited",
        "startDate":"Feb / 2022",
        "endDate":"Ongoing",
        "location":"Trivandrum",
        "description":"Worked closely with stakeholders to gather and analyze requirements for Microsoft Dynamics 365 CE solutions. Led workshops to understand business processes and translated them into functional specifications. Configured the Customer Service module and customized forms, views, dashboards, and security roles. Collaborated with developers to integrate Dynamics 365 with systems like SAP, GIS, and Yorbill. Contributed to Power Automate and Power Apps development, provided ongoing support, and recommended enhancements to improve business processes."
    }])

</script>
<style>
@import url(../../assets/styles/experence.scss);
</style>