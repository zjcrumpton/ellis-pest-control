<script>
  import { Router } from "@roxi/routify";
  import { routes } from "../.routify/routes";
  import Nav from "./components/Nav/Nav.svelte"
</script>

<style  global>
  @import "../assets/global.css";

  :global(*) {
    font-family: 'Roboto', sans-serif;
  }

  :global(html) {
    height: 100%;
    background: #161d25;
  }
</style>

<svelte:head>
  <title>Bed Bug Eliminators</title>
  <link rel="preconnect" href="https://fonts.gstatic.com">
  <link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet"> 
</svelte:head>

<Router {routes} />