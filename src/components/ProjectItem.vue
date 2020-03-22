<template>
    <div class="item">
        <div
            class="background-picture"
            :style="{
                backgroundImage: 'url(' + require(`@/assets/${image}`) + ')'
            }"
        ></div>
        <h3>{{ name }}</h3>
        <div class="info">
            <p class="subtitle">{{ subtitle }}</p>
            <i v-for="icon in icons" :class="[icon, 'colored']" :key="icon"></i>
            <p class="text">
                {{ description }}
            </p>
            <div class="links">
                <a :href="demoLink">Demo</a>
                <a :href="githubLink" class="source">GitHub</a>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    props: {
        name: String,
        subtitle: String,
        icons: Array,
        image: String,
        demoLink: String,
        githubLink: String,
        description: String
    }
};
</script>
<style scoped>
.item {
    padding: 1rem 1.5rem;
    box-shadow: 0 2px 4px 0 hsla(0, 0%, 0%, 0.15);
    background-color: #fbfbfb;
}

h3 {
    margin-top: 0.25rem;
    color: #4d538a;
}

.links {
    margin-top: 0.5rem;
}

a {
    position: relative;
    color: rgba(83, 83, 83, 0.808);
    text-decoration: none;
    margin-right: 0.85rem;
}

a::after {
    position: absolute;
    content: "";
    bottom: -3px;
    left: 0;
    height: 1px;
    width: 100%;
    border-color: rgba(66, 152, 151, 0.63);
    border-style: dashed;
    border-width: 0 0 2px 0;
}

a.source::after {
    border-color: rgba(249, 149, 56, 0.623);
}

.subtitle {
    font-size: 0.95rem;
    color: #4d5b8ad3;
    letter-spacing: 1px;
    margin-bottom: 0.75rem;
}

.info {
    max-width: 675px;
}

.background-picture {
    height: 250px;
    background-size: cover;
    background-repeat: no-repeat;
}

i {
    font-size: 2.5rem;
    margin-right: 0.5rem;
}
</style>
