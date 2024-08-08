<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin='true'>
<link href="https://fonts.googleapis.com/css2?family=Teko&family=Space+Grotesk:wght@300..700&display=swap" rel="stylesheet">

<script lang="ts">
    import { AppView } from "./types";
    import HomeView
     from "./views/home/HomeView.svelte";
  let view: AppView = AppView.Home;
  $: currentView = {
    [AppView.Home]: HomeView
  }[view];

</script>

<main>
  <svelte:component this={currentView} />
</main>

<style>
  main {
    display: flex;
    align-self: stretch;
    align-items: stretch;
    flex: 1 1 0px;
  }

</style>
