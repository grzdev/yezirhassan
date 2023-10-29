<script lang="ts">
  import ThemeSwitch from "$lib/ThemeSwitch/ThemeSwitch.svelte";
  import Icon from "@iconify/svelte";
  import { fade, fly } from "svelte/transition";
  import { onMount } from "svelte";
  import { createEventDispatcher } from "svelte";

  //  navbar function
  export let menuOpen: boolean;
  const dispatch = createEventDispatcher();
  let isMobileView = false;

  onMount(() => {
    const checkViewport = () => {
      isMobileView = window.innerWidth <= 768;
    };

    checkViewport();
    window.addEventListener("resize", checkViewport);
  });

  function toggleMenu() {
    menuOpen = !menuOpen;
    dispatch("toggleMenu");
  }

  function handleKeyDown(event: { key: string }) {
    if (event.key === "Escape") {
      toggleMenu();
    }
  }
</script>

<nav class="flex flex-row p-[2rem] items-center justify-between">
  <h1 class="text-4xl font-medium">.yh</h1>
  <!-- Navbar button -->
  {#if isMobileView && !menuOpen}
    <div class="md:hidden mt-[0.3rem]">
      <button on:click={toggleMenu}>
        <Icon
          icon="line-md:close-to-menu-alt-transition"
          class="text-black dark:text-[#d1d1d1] cursor-pointer text-3xl sm:text-3xl"
        />
      </button>
    </div>
  {:else}
    <div class="md:hidden mt-[0.3rem]">
      <button on:click={toggleMenu}>
        <Icon
          icon="line-md:menu-to-close-alt-transition"
          class="text-black dark:text-[#d1d1d1] cursor-pointer text-3xl sm:text-3xl"
        />
      </button>
    </div>
  {/if}
  <div class="flex flex-row items-center gap-[2.5rem] hidden md:flex">
    <div class="flex flex-row gap-[2.5rem] text-2xl font-semibold ml-[4rem]">
      <h1 class="dark:text-[#d1d1d1] dark:hover:text-white">Work</h1>
      <h1 class="dark:text-[#d1d1d1] dark:hover:text-white">About</h1>
      <h1 class="dark:text-[#d1d1d1] dark:hover:text-white">Resume</h1>
      <h1 class="dark:text-[#d1d1d1] dark:hover:text-white">More</h1>
    </div>
    <div class="flex flex-row items-center gap-[2rem]">
      <div
        class="w-[10rem] h-[2.5rem] bg-black dark:bg-[#d1d1d1] flex justify-center items-center rounded-xl"
      >
        <h1 class="text-[#d1d1d1] dark:text-black font-semibold text-xl">
          Get in touch
        </h1>
      </div>
      <ThemeSwitch />
    </div>
  </div>
</nav>

<!-- Sidebar content -->
{#if isMobileView}
  {#if menuOpen}
    <div class="fixed inset-0 z-50">
      <div
        class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8"
        on:click={toggleMenu}
        on:keydown={handleKeyDown}
        tabindex="-1"
        role="button"
        aria-label="Close"
      />
      <div
        class="w-full h-full md:w-64 bg-[#d1d1d1] dark:bg-[black] mt-[2rem]"
        in:fade={{ duration: 500 }}
        out:fade={{ duration: 700 }}
      >
        <div class="block md:hidden">
          <div class="flex flex-col gap-[2rem] items-center justify-center">
            <div class="flex flex-col gap-[2rem] items-center justify-center">
              <a
                href="/"
                class="text-black dark:text-[#d1d1d1] hover:text-white mt-[3rem] px-3 py-2 rounded-md text-3xl sm:text-4xl font-semibold"
                in:fly={{ y: 200, duration: 700 }}
                out:fly={{ y: 200, duration: 2000 }}>home</a
              >
              <a
                href="/projects"
                class="text-black dark:text-[#d1d1d1] hover:text-white px-3 py-2 rounded-md text-3xl sm:text-4xl font-semibold"
                in:fly={{ y: 200, duration: 1000 }}
                out:fly={{ y: 200, duration: 1500 }}>projects</a
              >
              <a
                href="/about"
                class="text-black dark:text-[#d1d1d1] hover:text-white px-3 py-2 rounded-md text-3xl sm:text-4xl font-semibold"
                in:fly={{ y: 200, duration: 1300 }}
                out:fly={{ y: 200, duration: 1000 }}>about</a
              >
              <a
                href="/contact"
                class="text-black dark:text-[#d1d1d1] hover:text-white px-3 py-2 rounded-md text-3xl sm:text-4xl font-semibold"
                in:fly={{ y: 200, duration: 1600 }}
                out:fly={{ y: 200, duration: 500 }}>contact</a
              >
            </div>
            <div />
          </div>
        </div>
      </div>
    </div>
  {/if}
{/if}
