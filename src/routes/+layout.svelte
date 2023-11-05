<!-- <script>
  import "../app.css";
</script> -->
<script>
  // @ts-ignore
  import { fly, fade, scale } from "svelte/transition";
  import { beforeNavigate, goto } from "$app/navigation";
  import "../app.css";

  let navigating = false;

  let onOutroendCb = () => {};

  beforeNavigate((navigation) => {
    if (!navigating) {
      navigating = true;
      navigation.cancel();
      onOutroendCb = async () => {
        // @ts-ignore
        const route = navigation.to.route.id;
        // @ts-ignore
        await goto(route);
        navigating = false;
      };
    }
  });

  // @ts-ignore
  let inDuration = 1000;
  // @ts-ignore
  let outDuration = 500;
</script>

<!-- <slot /> -->
<main>
  {#if !navigating}
    <div
      class="transition-wrapper"
      in:fade={{ duration: inDuration }}
      out:fade={{ duration: outDuration }}
      on:outroend={onOutroendCb}
    >
      <slot />
    </div>
  {/if}
</main>

<style>
  .transition-wrapper {
    grid-row: 1;
    grid-column: 1;
  }
</style>
