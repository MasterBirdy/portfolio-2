<template>
    <div id="app">
        <router-view />
    </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css?family=Ubuntu&display=swap");
@import url("https://fonts.googleapis.com/css?family=Lato&display=swap");
@import url("https://cdn.rawgit.com/konpa/devicon/df6431e323547add1b4cf45992913f15286456d3/devicon.min.css");
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Ubuntu, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    background-color: #fdfdfd;
    padding-bottom: 1rem;
}

#app {
    max-width: 900px;
    margin: 2rem auto 0;
    padding: 0 20px;
}

.text {
    color: rgb(24, 24, 24);
    font-size: 1rem;
    margin-top: 0.5rem;
    line-height: 1.44;
}
</style>
