<template>
    <div>
        <div class="nav-grid">
            <Header></Header>
            <NavBar></NavBar>
        </div>
        <AboutMe></AboutMe>
        <Skills></Skills>
        <Projects></Projects>
    </div>
</template>

<script>
import Header from "@/components/Header";
import NavBar from "@/components/NavBar";
import AboutMe from "@/components/AboutMe";
import Skills from "@/components/Skills";
import Projects from "@/components/Projects";
// @ is an alias to /src

export default {
    name: "Home",
    components: {
        Header,
        NavBar,
        AboutMe,
        Skills,
        Projects
    }
};
</script>
<style>
.nav-grid {
    display: grid;
    grid-template-columns: 1fr 2fr;
}

p {
    font-size: 1rem;
}
</style>
