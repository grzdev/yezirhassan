<script lang="ts">
  import Page from "$lib/Page.svelte";
  import ThemeSwitch from "$lib/ThemeSwitch/ThemeSwitch.svelte";

  import "../app.css";
  import LoadScreen from "../components/LoadScreen.svelte";
  import Navbar from "../components/Navbar.svelte";
  import Home from "../modules/Home.svelte";
  let menuOpen = false;

  // LoadScreen
  let isLoading = true;
  setTimeout(() => {
    isLoading = false;
  }, 2000);
</script>

{#if isLoading}
  <LoadScreen />
{:else}
  <div>
    <Navbar {menuOpen} on:toggleMenu={() => (menuOpen = !menuOpen)} />
    <Home />
  </div>
{/if}

<style>
</style>
