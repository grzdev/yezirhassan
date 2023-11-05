<script lang="ts">
  import ThemeSwitch from "$lib/ThemeSwitch/ThemeSwitch.svelte";
  import Icon from "@iconify/svelte";
  import { fade, fly } from "svelte/transition";
  import { onMount } from "svelte";
  import { createEventDispatcher } from "svelte";
  import Logo from "../image/logo2.png";
  import LogoDark from "../image/logo3.png";

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

  // logo switch
</script>

<nav
  class="flex flex-row p-[1rem] sm:p-[2rem] md:p-[2rem] items-center justify-between"
>
  <div>
    <img
      id="logoDark"
      src={LogoDark}
      alt=""
      class="w-[6rem] sm:w-[8rem] md:w-[9rem] brightness-120 dark:brightness-130"
    />
  </div>
  <!-- Navbar button -->
  {#if isMobileView && !menuOpen}
    <div class="md:hidden mt-[0.3rem]">
      <button on:click={toggleMenu}>
        <Icon
          icon="line-md:close-to-menu-alt-transition"
          class="text-[#6a6868] dark:text-[#989898] cursor-pointer text-3xl sm:text-3xl"
        />
      </button>
    </div>
  {:else}
    <div class="md:hidden mt-[0.3rem]">
      <button on:click={toggleMenu}>
        <Icon
          icon="line-md:menu-to-close-alt-transition"
          class="text-[#6a6868] dark:text-[#989898] cursor-pointer text-3xl sm:text-3xl"
        />
      </button>
    </div>
  {/if}
  <div
    class="flex flex-row items-center gap-[2.5rem] hidden md:flex mt-[-2rem]"
  >
    <div class="flex flex-row gap-[2.5rem] text-xl font-semibold ml-[4rem]">
      <a href="work">
        <h1
          class="text-[#6a6868] dark:text-[#989898] hover:text-black dark:hover:text-white transition duration-500 ease-in-out page1"
        >
          Work
        </h1>
      </a>
      <a href="about">
        <h1
          class="text-[#6a6868] dark:text-[#989898] hover:text-black dark:hover:text-white transition duration-500 ease-in-out page2"
        >
          About
        </h1>
      </a>
      <h1
        class="text-[#6a6868] dark:text-[#989898] hover:text-black dark:hover:text-white transition duration-500 ease-in-out page3"
      >
        Resume
      </h1>
      <a href="more">
        <h1
          class="text-[#6a6868] dark:text-[#989898] hover:text-black dark:hover:text-white transition duration-500 ease-in-out page4"
        >
          More
        </h1>
      </a>
    </div>
    <div class="flex flex-row items-center gap-[2rem]">
      <a href="/contact">
        <div
          class="page5 w-[10rem] h-[3rem] bg-[#35a35b] dark:bg-[#2E9953] hover:bg-[#24673b] dark:hover:bg-[#3bc26a] transition duration-500 ease-in-out flex justify-center items-center rounded-xl"
        >
          <h1 class="text-[white] dark:text-white font-semibold text-xl">
            Get in touch
          </h1>
        </div>
      </a>
      <div class="darkmode mr-[3rem]">
        <ThemeSwitch />
      </div>
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
        class="w-full h-full md:w-64 bg-[#dfdfdf] dark:bg-[black] mt-[2rem]"
        in:fade={{ duration: 500 }}
        out:fade={{ duration: 700 }}
      >
        <div class="block md:hidden">
          <div class="flex flex-col gap-[2rem] items-center justify-center">
            <div class="flex flex-col gap-[2rem] items-center justify-center">
              <a
                href="/"
                class="text-[#6a6868] dark:text-[#989898] hover:text-black dark:hover:text-white transition duration-500 ease-in-out mt-[3rem] px-3 py-2 rounded-md text-2xl sm:text-3xl font-semibold"
                in:fly={{ y: 200, duration: 700 }}
                out:fly={{ y: 200, duration: 2000 }}>Work</a
              >
              <a
                href="/work"
                class="text-[#6a6868] dark:text-[#989898] hover:text-black dark:hover:text-white transition duration-500 ease-in-out px-3 py-2 rounded-md text-2xl sm:text-3xl font-semibold"
                in:fly={{ y: 200, duration: 1000 }}
                out:fly={{ y: 200, duration: 1500 }}>About</a
              >
              <a
                href="/about"
                class="text-[#6a6868] dark:text-[#989898] hover:text-black dark:hover:text-white transition duration-500 ease-in-out px-3 py-2 rounded-md text-2xl sm:text-3xl font-semibold"
                in:fly={{ y: 200, duration: 1300 }}
                out:fly={{ y: 200, duration: 1000 }}>Resume</a
              >
              <a
                href="/more"
                class="text-[#6a6868] dark:text-[#989898] hover:text-black dark:hover:text-white transition duration-500 ease-in-out px-3 py-2 rounded-md text-2xl sm:text-3xl font-semibold"
                in:fly={{ y: 200, duration: 1600 }}
                out:fly={{ y: 200, duration: 500 }}>More</a
              >
            </div>
            <div class="flex flex-col items-center gap-[2rem]">
              <a href="/contact">
                <div
                  class="w-[10rem] h-[3rem] bg-[#146631] dark:hover:text-white flex justify-center items-center rounded-xl"
                  in:fly={{ y: 200, duration: 1900 }}
                  out:fly={{ y: 200, duration: 300 }}
                >
                  <h1
                    class=" text-[white] dark:text-white font-semibold text-xl"
                  >
                    Get in touch
                  </h1>
                </div>
              </a>
              <div
                in:fly={{ y: 200, duration: 1900 }}
                out:fly={{ y: 200, duration: 300 }}
              >
                <ThemeSwitch />
              </div>
            </div>
            <div />
          </div>
        </div>
      </div>
    </div>
  {/if}
{/if}

<style>
  @keyframes slideFromTop {
    0% {
      transform: translateY(-100%);
    }
    100% {
      transform: translateY(0);
    }
  }

  @keyframes moveFromBottomRight2 {
    0% {
      transform: translate(10%, 10%);
      opacity: 0;
    }
    100% {
      transform: translate(0, 0);
      opacity: 1;
    }
  }
  .logo {
    animation: moveFromBottomRight2 1s ease-in-out;
  }
  .page1 {
    animation: slideFromTop 0.5s ease-in-out;
    transform: translateY(100);
  }
  .page2 {
    animation: slideFromTop 0.7s ease-in-out;
    transform: translateY(100);
  }
  .page3 {
    animation: slideFromTop 0.8s ease-in-out;
    transform: translateY(100);
  }
  .page4 {
    animation: slideFromTop 0.9s ease-in-out;
    transform: translateY(100);
  }
  .page5 {
    animation: slideFromTop 1s ease-in-out;
    transform: translateY(100);
  }
  .text-bounce {
    transition: transform 0.2s ease-in-out;
  }
</style>
