<template>
    <div id="aboutMe">
        <h2>About Me</h2>
        <p class="text">
            Hi, I'm Matthew! I'm a full stack web developer. I love creating
            beautiful websites with the newest technology and modern frameworks
            and languages including <span class="bold">JavaScript</span>,
            <span class="bold2">Vue</span>, and
            <span class="bold3">NodeJS</span>.
        </p>
        <p class="text">
            When I'm not programming, I enjoy playing computer games, running,
            and watching movies.
        </p>
    </div>
</template>
<script>
export default {};
</script>
<style scoped>
.text {
    margin-bottom: 1.5rem;
}

#aboutMe {
    margin-top: 5rem;
    max-width: 500px;
}

h2 {
    font-size: 1.32rem;
    color: #3a6dcccc;
}

.bold {
    color: rgba(25, 17, 92, 0.767);
    font-weight: 600;
}

.bold2 {
    color: rgba(14, 124, 122, 0.808);
    font-weight: 600;
}

.bold3 {
    color: rgba(248, 162, 2, 0.808);
    font-weight: 600;
}
</style>
