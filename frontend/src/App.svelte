<script lang="ts">
  import "./app.css";
  import '@fontsource/geist-sans/700.css';
  import '@fontsource/geist-mono/700.css';
  import Grid from './lib/Grid.svelte'
  import Footer from './lib/Footer.svelte';
  import Stats from './lib/Stats.svelte';
</script>

<main>
  <h1 class="header font-bold">Rewilding Planner</h1>
  <div class="relative flex flex-col items-center p-6">
    <div class="stats-container">
      <Stats />
    </div>
    <Grid />
  </div>
  <Footer />
</main>
<style>
  :root {
    overflow: hidden;
  }
  .header {
    font-family: 'Geist Sans', Helvetica, sans-serif;
  }
  .stats-container {
    position: absolute;
    display: flex;
    justify-content: end;
    width: 1475px;
    max-width: calc(100vw - 2rem);
  }
  @media (max-width: 1450px) {
    .stats-container {
      position: relative;
      justify-content: center;
    }
  }
</style>
