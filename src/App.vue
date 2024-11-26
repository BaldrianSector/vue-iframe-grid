<template>
  <div id="app">
      <h1>Netlify Deployed Projects</h1>
      <IframeGrid />
  </div>
</template>

<script>
import IframeGrid from './components/IframeGrid.vue';

export default {
  components: {
      IframeGrid,
  },
};
</script>

<style>
#app {
  font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
  line-height: 1.5;
  font-weight: 400;
  text-align: center;
  background-color: #242424; /* Match the background color */
  color: rgba(255, 255, 255, 0.87); /* Text color */
  padding: 32px; /* Space around the content */
  height: 1200px;
}

h1 {
  font-size: 2.5em;
  margin-bottom: 24px;
  color: #ffffff; /* Highlighted header color */
}
</style>
