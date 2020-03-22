<template>
    <nav>
        <ul>
            <li v-for="link in links" :key="link.text">
                <a :href="link.link">{{ link.text }}</a>
            </li>
        </ul>
        <div class="hamburger"></div>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            links: [
                {
                    text: "About Me",
                    link: "#aboutMe"
                },
                {
                    text: "Skills",
                    link: "#skills"
                },
                {
                    text: "Projects",
                    link: "#projects"
                },
                {
                    text: "Contact",
                    link: "#contact"
                },
                {
                    text: "Resume",
                    link: "#resume"
                }
            ]
        };
    }
};
</script>
<style scoped>
nav {
    display: flex;
    justify-content: flex-end;
}

p {
    color: rgba(25, 17, 92, 0.664);
    font-size: 1.05rem;
}

ul {
    list-style: none;
    display: flex;
}

li {
    font-weight: 500;
    margin-left: 2.25rem;
    align-self: center;
}

a,
a:visited {
    position: relative;
    text-decoration: none;
    color: rgba(25, 17, 92, 0.664);
    transition: all 1s ease-in-out;
}

a:hover,
a:active {
    color: rgba(12, 98, 196, 0.651);
}

a::after {
    position: absolute;
    content: "";
    bottom: -3px;
    left: 0;
    width: 0%;
    height: 1px;
    background-color: rgba(25, 17, 92, 0.342);
    transition: all 1s ease-in;
}

a:hover::after,
a:active::after {
    width: 100%;
}

.hamburger {
    display: none;
    position: absolute;
    width: 35px;
    height: 4px;
    background-color: rgba(25, 17, 92, 0.664);
    border-radius: 10px;
    right: 18px;
    top: 36px;
}

.hamburger::before {
    position: absolute;
    width: 35px;
    height: 4px;
    content: "";
    background-color: rgba(25, 17, 92, 0.664);
    border-radius: 5px;
    right: 0;
    top: -8px;
}

.hamburger::after {
    position: absolute;
    width: 35px;
    height: 4px;
    content: "";
    background-color: rgba(25, 17, 92, 0.664);
    border-radius: 10px;
    right: 0;
    bottom: -8px;
}

@media (max-width: 768px) {
    .hamburger {
        display: block;
    }

    ul {
        display: none;
    }
}
</style>
