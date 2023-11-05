<script>
  import Page from "$lib/Page.svelte";
  import Navbar from "../../components/Navbar.svelte";
  import About from "../../modules/About.svelte";
  let menuOpen = false;
</script>

<Page>
  <Navbar {menuOpen} on:toggleMenu={() => (menuOpen = !menuOpen)} />
  <About />
</Page>
