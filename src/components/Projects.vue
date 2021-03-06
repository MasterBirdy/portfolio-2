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
                :imageLink="project.imageLink"
                :hasGithub="project.githubLink !== null"
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
                    name: "Moving Mindz",
                    subtitle: "Educational Python App",
                    icons: [
                        "devicon-react-original-wordmark",
                        "devicon-nodejs-plain-wordmark colored",
                        "devicon-sass-original colored",
                        "devicon-mysql-plain colored"
                    ],
                    image: "movingminds.png",
                    demoLink: "https://www.movingmindz.xyz",
                    githubLink: null,
                    imageLink:
                        "https://images-masterbirdy.s3-us-west-1.amazonaws.com/movingminds.png",
                    description:
                        "A full stack web application created with React and Hapi designed for students to learn Python through lessons using the Turtle library with a STEM-focused curriculum."
                },
                {
                    name: "VRMS",
                    subtitle: "Volunteer Relationship Management System",
                    icons: [
                        "devicon-react-original-wordmark",
                        "devicon-nodejs-plain-wordmark colored",
                        "devicon-express-original-wordmark colored",
                        "devicon-mongodb-plain-wordmark colored"
                    ],

                    image: "vrms-resized.jpg",
                    demoLink: "https://www.vrms.io/",
                    githubLink: "https://github.com/hackforla/VRMS",
                    imageLink:
                        "https://images-masterbirdy.s3-us-west-1.amazonaws.com/vrms.jpg",
                    description:
                        "An open-source React project from Hack for LA that will be used by the organization to engage, support, and retain a network of volunteers for future open-source projects."
                },
                {
                    name: "Pokedex",
                    subtitle: "Pokemon App",
                    icons: [
                        "devicon-html5-plain",
                        "devicon-css3-plain",
                        "devicon-javascript-plain",
                        "devicon-react-original-wordmark"
                    ],
                    image: "pokedex-resized.png",
                    demoLink: "https://fervent-leavitt-5ba39c.netlify.app",
                    githubLink: "https://github.com/MasterBirdy/pokedex",
                    imageLink:
                        "https://images-masterbirdy.s3-us-west-1.amazonaws.com/pokedex-compressor.png",
                    description:
                        "A React App utilizing React Hooks, Material UI, and PokeAPI to pull up information including Pokemon moves, stats, and description. It also displays a type effectiveness chart."
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
                    imageLink:
                        "https://images-masterbirdy.s3-us-west-1.amazonaws.com/catblog-compressed.jpg",
                    description:
                        "A Vue application powered by Netlify CMS that lets users write blog posts about their favorite feline companions."
                },
                {
                    name: "Country Viewer",
                    subtitle: "REST API Country List",
                    icons: [
                        "devicon-html5-plain",
                        "devicon-css3-plain",
                        "devicon-javascript-plain",
                        "devicon-vuejs-plain"
                    ],
                    image: "rest-countries-resized.jpg",
                    demoLink: "https://awesome-colden-14cbac.netlify.com/",
                    githubLink: "https://github.com/MasterBirdy/rest-countries",
                    imageLink:
                        "https://images-masterbirdy.s3-us-west-1.amazonaws.com/rest-countries-compressed.png",
                    description:
                        "A Vue application using the REST Countries API to complete a front end challenge by Frontend Mentor, replicating UI design specifications to make a country data viewer."
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
    padding-top: 1rem;
    margin-top: 3.75rem;
}

h2 {
    text-transform: lowercase;
    font-size: 1.35rem;
    color: #3a6dcccc;
}

.project-grid {
    margin-top: 0.65rem;
    padding: 0 0.5rem;
    display: grid;
    grid-template-columns: 1fr;
    grid-row-gap: 2.5rem;
}

.button-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
}

@media (max-width: 768px) {
    h2 {
        font-size: 1.32rem;
    }
}
</style>
