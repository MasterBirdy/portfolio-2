<template>
    <div id="projects">
        <h2>Projects</h2>
        <div class="project-grid">
            <ProjectItem :name="'KaoBook'"></ProjectItem>
            <ProjectItem :name="'test'"></ProjectItem>
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
    margin-top: 1rem;
    padding: 0 0.5rem;
    display: grid;
    grid-template-columns: 1fr;
    grid-row-gap: 2.5rem;
}

.button-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
}
</style>
