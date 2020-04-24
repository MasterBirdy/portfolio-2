<template>
    <div id="aboutMe">
        <h2>About Me</h2>
        <p class="text">
            Hi, I'm Matthew! I'm a full stack web developer. I love creating
            beautiful websites with the newest technology and modern frameworks
            and languages including <span class="bold3">NodeJS</span>,
            <span class="bold4">React</span>, <span class="bold2">Vue</span>,
            and <span class="bold">JavaScript</span>.
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
    margin-top: 4rem;
    padding-top: 1rem;
    max-width: 500px;
}

h2 {
    font-size: 1.35rem;
    color: #3a6dcccc;
    text-transform: lowercase;
    letter-spacing: 1px;
}

.bold3 {
    color: rgba(96, 163, 15, 0.808);
    font-weight: 600;
}

.bold2 {
    color: rgba(14, 124, 122, 0.808);
    font-weight: 600;
}

.bold {
    color: rgba(202, 139, 21, 0.808);
    font-weight: 600;
}

.bold4 {
    color: #39badd;
    font-weight: 600;
}

@media (max-width: 768px) {
    h2 {
        font-size: 1.32rem;
    }
}
</style>
