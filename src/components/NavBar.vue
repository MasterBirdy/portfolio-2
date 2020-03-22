<template>
    <nav>
        <ul>
            <li>
                <a href="#aboutMe">About Me</a>
            </li>
            <li>
                <a href="#skills">Skills</a>
            </li>
            <li>
                <a href="#projects">Projects</a>
            </li>
            <li>
                <a href="#contact">Contact</a>
            </li>
            <li>
                <p>Resume</p>
            </li>
        </ul>
    </nav>
</template>

<script></script>
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
</style>
