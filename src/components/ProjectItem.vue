<template>
    <div class="item">
        <div class="background-picture"></div>
        <h3>{{ name }}</h3>
        <div class="info">
            <p class="subtitle">Social Media App</p>
            <i class="devicon-nodejs-plain colored"></i>
            <i class="devicon-express-original-wordmark colored"></i>
            <i class="devicon-mongodb-plain-wordmark colored"></i>
            <i class="devicon-vuejs-plain colored"></i>
            <p class="text">
                A full stack web application with social login and timelines to
                let you write posts and comments on your friends' pages.
            </p>
        </div>
    </div>
</template>
<script>
export default {
    props: {
        name: String
    }
};
</script>
<style scoped>
h3 {
    margin-top: 0.25rem;
    color: #4d538a;
}

.subtitle {
    font-size: 0.95rem;
    color: #4d5b8ad3;
    letter-spacing: 1px;
    margin-bottom: 0.75rem;
}

.item {
    padding: 1rem 1.5rem;
    box-shadow: 0 2px 4px 0 hsla(0, 0%, 0%, 0.15);
}

.info {
    max-width: 675px;
}

.background-picture {
    height: 250px;
    background-image: url("~@/assets/kaobook-resized.jpg");
    background-size: cover;
    background-repeat: no-repeat;
}

i {
    font-size: 2.5rem;
    margin-right: 0.5rem;
}
</style>
