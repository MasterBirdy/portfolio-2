<template>
    <div>
        <h1>Matthew Ito</h1>
        <p class="subtitle">Full stack web developer</p>
    </div>
</template>

<script>
// @ is an alias to /src

export default {
    name: "Home"
};
</script>
<style scoped>
div {
    margin-top: 2rem;
}

h1 {
    color: rgb(24, 17, 92);
    text-transform: lowercase;
}
.subtitle {
    color: rgba(44, 36, 129, 0.726);
    letter-spacing: 1px;
    text-transform: lowercase;
}

@media (max-width: 768px) {
    div {
        margin-top: 1.25rem;
    }
}
</style>
