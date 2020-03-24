<template>
    <div id="contact">
        <h2>Contact Me</h2>
        <p class="text">
            Feel free to either send me an e-mail at
            <a href="mailto:hello@mattito.dev">hello@mattito.dev</a> or to send
            a message with the form below! Thanks for coming by! 👋
        </p>
        <form id="form" name="form" netlify>
            <label for="name">Name</label>
            <input type="text" id="name" name="name" />
            <label for="email">Email</label>
            <input type="text" id="email" name="email" />
            <label for="message">Message</label>
            <textarea id="message" name="message" rows="4" />
            <button type="submit" form="form" value="Submit">Submit</button>
        </form>
    </div>
</template>
<script>
export default {};
</script>
<style scoped>
#contact {
    padding-top: 1rem;
    margin-top: 1.25rem;
    max-width: 500px;
}
h2 {
    font-size: 1.35rem;
    color: #3a6dcccc;
    text-transform: lowercase;
}
input,
textarea {
    display: block;
    margin-bottom: 0.66rem;
    padding: 0.3rem 0.25rem;
    font-size: 0.9rem;
    border: 1px solid rgb(170, 170, 170);
    font-family: "Ubuntu", sans-serif;
    width: 80%;
}

label {
    display: block;
    margin-bottom: 0.25rem;
    color: rgba(37, 29, 117, 0.726);
    font-size: 0.98rem;
    letter-spacing: 1px;
    font-family: "Ubuntu", sans-serif;
    text-transform: lowercase;
}

form {
    margin-top: 0.7rem;
}

button {
    margin-top: 0.25rem;
    cursor: pointer;
    padding: 0.25rem 0.5rem;
    font-size: 0.9rem;
    border: 1px solid rgb(170, 170, 170);
    font-family: "Ubuntu", sans-serif;
}

a {
    color: rgba(25, 17, 92, 0.795);
    text-decoration: none;
}

@media (max-width: 768px) {
    textarea,
    input,
    label {
        width: 100%;
    }

    h2 {
        font-size: 1.32rem;
    }
}
</style>
