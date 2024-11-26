<template>
    <div class="grid-container">
        <IframeCard
            v-for="(site, index) in websites"
            :key="index"
            :name="site.name"
            :url="site.url"
        />
    </div>
</template>

<script>
import IframeCard from './IframeCard.vue';

export default {
    components: {
        IframeCard,
    },
    data() {
        return {
            websites: [],
        };
    },
    created() {
        fetch('src/assets/websites.json')
            .then(response => response.json())
            .then(data => {
                this.websites = data;
            });
    },
};
</script>

<style scoped>
.grid-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr); /* 2x2 grid */
    gap: 16px; /* Space between grid items */
    padding: 16px; /* Space around the grid */
    margin: 0 auto; /* Center grid horizontally */
    background-color: #242424; /* Match the dark background */
    border-radius: 8px; /* Slight rounding for aesthetics */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Subtle shadow for elevation */
    
    transform: scale(0.8);
    transform-origin: top center;
}
</style>
