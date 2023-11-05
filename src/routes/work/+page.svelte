<script>
  import Page from "$lib/Page.svelte";
  import Navbar from "../../components/Navbar.svelte";
  import Work from "../../modules/Work.svelte";

  let menuOpen = false;
</script>

<div>
  <Navbar {menuOpen} on:toggleMenu={() => (menuOpen = !menuOpen)} />
  <Work />
</div>
