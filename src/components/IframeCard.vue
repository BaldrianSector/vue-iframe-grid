<template>
    <div class="card">
        <h3>
            <a :href="url" target="_blank" rel="noopener noreferrer">{{ name }}</a>
        </h3>
        <iframe
            :src="url"
            frameborder="0"
            class="iframe"
            allowfullscreen
        ></iframe>
    </div>
</template>

<script>
export default {
    props: {
        name: {
            type: String,
            required: true,
        },
        url: {
            type: String,
            required: true,
        },
    },
};
</script>

<style>
.card {
    width: 500px;
    height: 548px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border: 1px solid #838383;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    overflow: hidden;
}

h3 {
    margin: 8px 0;
    font-size: 1.2rem;
    text-align: center;
}

h3 a {
    color: inherit;
}

h3 a:hover {
    text-decoration: underline;
    color: white;
}

.iframe {
    width: 100%;
    height: 100%; /* Full height minus the heading space */
    border: none;
}
</style>