<template>
    <div id="projects">
        <h2>Projects</h2>
        <div class="project-grid">
            <ProjectItem
                v-for="project in projects"
                :key="project.name"
                :name="project.name"
                :subtitle="project.subtitle"
                :icons="project.icons"
                :image="project.image"
                :demoLink="project.demoLink"
                :githubLink="project.githubLink"
                :description="project.description"
            ></ProjectItem>
        </div>
        <div class="button-grid">
            <div class="button-flex"></div>
            <div class="button-flex"></div>
        </div>
    </div>
</template>
<script>
import ProjectItem from "@/components/ProjectItem";

export default {
    data() {
        return {
            projects: [
                {
                    name: "KaoBook",
                    subtitle: "Social Media App",
                    icons: [
                        "devicon-nodejs-plain",
                        "devicon-express-original-wordmark",
                        "devicon-mongodb-plain-wordmark",
                        "devicon-vuejs-plain"
                    ],
                    image: "kaobook-resized.jpg",
                    demoLink: "http://138.68.2.3/",
                    githubLink: "https://github.com/MasterBirdy/kaobook-server",
                    description:
                        "A full stack web application with social login and timelines to let you write posts and comments on your friends' pages."
                },
                {
                    name: "Cat Blog",
                    subtitle: "Netlify CMS Blog",
                    icons: [
                        "devicon-html5-plain",
                        "devicon-css3-plain",
                        "devicon-javascript-plain",
                        "devicon-vuejs-plain"
                    ],
                    image: "catblog-resized.jpg",
                    demoLink: "https://objective-dijkstra-75b79d.netlify.com/",
                    githubLink: "https://github.com/MasterBirdy/crispy-eureka",
                    description:
                        "A Vue application powered by Netlify CMS that lets users write blogs about their favorite feline companions."
                }
            ]
        };
    },
    components: {
        ProjectItem
    }
};
</script>
<style scoped>
#projects {
    margin-top: 4.75rem;
}

h2 {
    font-size: 1.32rem;
    color: #3a6dcccc;
}

.project-grid {
    margin-top: 0.8rem;
    padding: 0 0.5rem;
    display: grid;
    grid-template-columns: 1fr;
    grid-row-gap: 2.25rem;
}

.button-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
}
</style>
