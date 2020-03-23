<template>
    <nav>
        <div class="menu-wrap">
            <input type="checkbox" class="toggler" />
            <div class="hamburger"></div>
            <div class="circle"></div>
            <div class="menu">
                <ul>
                    <li v-for="link in links" :key="link.text">
                        <a :href="link.link" @click="mobileClose">{{
                            link.text
                        }}</a>
                    </li>
                </ul>
            </div>
        </div>
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
    },
    methods: {
        mobileClose() {
            if (window.innerWidth <= 768) {
                document.querySelector("input[type=checkbox]").checked = false;
            }
        }
    }
};
</script>
<style scoped>
nav {
    display: flex;
    justify-content: flex-end;
}

.menu-wrap {
    position: relative;
    top: 52%;
    right: 10px;
}

p {
    color: rgba(25, 17, 92, 0.664);
    font-size: 1.05rem;
}

ul {
    list-style: none;
    display: flex;
    z-index: 2;
}

li {
    font-weight: 500;
    margin-left: 2.25rem;
    align-self: center;
}

a,
a:visited {
    font-family: "Ubuntu", sans-serif;
    letter-spacing: 1px;
    position: relative;
    text-decoration: none;
    color: rgba(25, 17, 92, 0.726);
    transition: color 1s ease-in-out;
    text-transform: lowercase;
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

.toggler {
    position: absolute;
    top: 0;
    right: 0;
    z-index: 3;
    cursor: pointer;
    width: 55px;
    height: 55px;
    opacity: 0;
    pointer-events: none;
}

.hamburger {
    display: none;
    position: relative;
    width: 35px;
    height: 4px;
    background-color: rgba(25, 17, 92, 0.664);
    border-radius: 10px;
    right: 18px;
    top: 36px;
    transition: all 0.5s ease;
    z-index: 2;
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
    z-index: 2;
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
    z-index: 2;
}

.menu-wrap .toggler:checked ~ .hamburger {
    transform: rotate(135deg);
    background-color: rgba(25, 17, 92, 1);
}

.menu-wrap .toggler:checked ~ .hamburger::before {
    top: 0;
    transform: rotate(90deg);
    background-color: rgba(25, 17, 92, 1);
}

.menu-wrap .toggler:checked ~ .hamburger::after {
    opacity: 0;
    background-color: rgba(25, 17, 92, 1);
    top: 0;
    transform: rotate(90deg);
}

.circle {
    background-color: rgba(56, 50, 116, 0.8);
    border-radius: 50%;
    width: 100vw;
    height: 100vw;
    position: fixed;
    left: 50%;
    top: 50%;
    opacity: 1;
    transform: translate(-50%, -50%) scale(0);
    transition: all 0.8s ease;
}

.toggler:checked ~ .circle {
    opacity: 1;
    transform: translate(-50%, -50%) scale(2.5);
}

@media (max-width: 768px) {
    .menu-wrap {
        position: fixed;
        top: 0;
        right: 0;
        z-index: 1;
    }

    .hamburger {
        display: block;
    }
    .menu {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        flex-direction: column;
        display: flex;
        align-content: center;
        justify-content: center;
        pointer-events: none;
    }

    ul {
        text-align: center;
        flex-direction: column;
        height: 65%;
        justify-content: space-around;
    }

    li {
        margin-left: 0;
    }

    a,
    a:visited,
    a:hover,
    a:active {
        color: white;
        opacity: 0;
        font-size: 1.6rem;
        font-family: "Lato", sans-serif;
        font-weight: 400;
        letter-spacing: 2px;
        text-transform: lowercase;
        transition: opacity 0.4s ease;
    }

    a::after {
        background-color: white;
    }

    .toggler:checked ~ div a {
        opacity: 1;
    }

    .toggler {
        pointer-events: auto;
    }

    .toggler:checked ~ .menu {
        pointer-events: auto;
    }
}
</style>
