<template>
    <div>
        <main class="fillHeight firstpage">
            <PersonalDetails></PersonalDetails>
            <AboutMe></AboutMe>
            <ExpericenceAndProjects></ExpericenceAndProjects>
            <ContactMe></ContactMe>
        </main>
        <footer class="footer-class">
            <div class="footer-div">
                <h2 class="footer-heading">Krishnaja V</h2>
            </div>
            <div class="footer-div">
                <div class="footer-content">Designed & Built by <span> <a href="https://www.linkedin.com/in/krishnajith-career/" aria-label="LinkedIn" target="_blank" rel="noreferrer"> Krishnajith</a></span></div>
            </div>
            <div class="footer-social-media">
                <div>
                    <a href="https://github.com/krishnajaV" aria-label="GitHub" target="_blank" rel="noreferrer">
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 24 24"
                            fill="none"
                            class="feather feather-github"
                            stroke="currentColor"
                            stroke-width="2"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            role="img">
                            <title>GitHub</title>
                            <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22" />
                        </svg>
                    </a>
                </div>
                <div>
                    <a href="https://www.instagram.com/krishnaja_ranjith/" aria-label="Instagram" target="_blank" rel="noreferrer">
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 24 24"
                            fill="none"
                            class="feather feather-instagram"
                            stroke="currentColor"
                            stroke-width="2"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            role="img">
                            <title>Instagram</title>
                            <rect x="2" y="2" width="20" height="20" rx="5" ry="5" />
                            <path d="M16 11.5a4.5 4.5 0 1 1-9 0 4.5 4.5 0 0 1 9 0z" />
                            <line x1="17.5" y1="6.5" x2="17.5" y2="6.5" />
                        </svg>
                    </a>
                </div>
                <div>
                    <a href="https://www.linkedin.com/in/krishnaja-v-8409941b3/" aria-label="Linked In" target="_blank" rel="noreferrer">
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 24 24"
                            fill="none"
                            stroke="currentColor"
                            stroke-width="2"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            class="feather feather-linkedin"
                            role="img">
                            <title>LinkedIn</title>
                            <path d="M16 8a6 6 0 0 1 6 6v8h-4v-8a2 2 0 0 0-4 0v8h-4v-8a6 6 0 0 1 6-6z" />
                            <rect x="2" y="9" width="4" height="12" />
                            <circle cx="4" cy="4" r="2" />
                        </svg>
                    </a>
                </div>
            </div>
        </footer>
    </div>
</template>
<script setup>
    import PersonalDetails from './PersonalDetails.vue'; 
    import AboutMe from './AboutMe.vue';
    import ExpericenceAndProjects from './ExpericenceAndProjects.vue'
    import ContactMe from './ContactMe.vue';
</script>
<style >
    @import '../../assets/styles/mainPage.scss';
</style>
