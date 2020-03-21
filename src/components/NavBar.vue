<template>
    <nav>
        <ul>
            <li>
                <p>About Me</p>
            </li>
            <li>
                <p>Skills</p>
            </li>
            <li>
                <p>Projects</p>
            </li>
            <li>
                <p>Contact</p>
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
</style>
