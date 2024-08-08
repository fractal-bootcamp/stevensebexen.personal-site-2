<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin='anonymous'>
<link href="https://fonts.googleapis.com/css2?family=Teko&family=Space+Grotesk:wght@300..700&display=swap" rel="stylesheet">

<script lang="ts">
    import { AppView } from "./types";
    import HomeView from "./views/home/HomeView.svelte";
    import NavigationView from "./views/navigation/NavigationView.svelte";
  let view: AppView = AppView.Home;
  const viewComponents = {
    [AppView.Home]: HomeView,
    [AppView.Navigation]: NavigationView
  };
  $: viewComponent = viewComponents[view]

  function changeView(e: CustomEvent<AppView>) {
    view = e.detail;
  }
</script>

<main>
  <svelte:component this={viewComponent} on:changeview={changeView} />
</main>

<style>
  main {
    display: flex;
    align-self: stretch;
    flex: 1 1 0px;
  }

</style>
