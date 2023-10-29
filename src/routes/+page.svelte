<script lang="ts">
  import ThemeSwitch from "$lib/ThemeSwitch/ThemeSwitch.svelte";

  import "../app.css";
  import Navbar from "../components/Navbar.svelte";
  import Home from "../modules/Home.svelte";
  let menuOpen = false;
</script>

<div>
  <Navbar {menuOpen} on:toggleMenu={() => (menuOpen = !menuOpen)} />
  <Home />
</div>

<style>
</style>
