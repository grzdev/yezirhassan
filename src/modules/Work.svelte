<script lang="ts">
  import { fade } from "svelte/transition";
  import WorkCard from "../components/WorkCard.svelte";
  import featuredWork from "../components/featuredWork.json";
  import type { Work } from "../components/workInterface";
  export let work: Work[] = featuredWork.work;
</script>

<div class="flex justify-center items-center">
  <div class="flex flex-col overflow-x-hidden px-[1rem]">
    <h2
      class="move-from-buttom hover:text-black dark:hover:text-white transition duration-500 ease-in-out text-[2rem] sm:text-[4rem] md:text-[5rem] lg:text-[5rem] font-bold text-[#6a6868] dark:text-[#989898] mt-[-0.2rem] sm:mt-[-0.7rem] md:mt-[-2rem]"
    >
      Featured Work
    </h2>
    <div
      class="flex flex-row gap-[2rem] sm:gap-[3rem] md:gap-[3rem] p-[1rem] overflow-x-auto custom-scrollbar mt-[-1rem] move-container"
    >
      <WorkCard {work} />
    </div>
  </div>
</div>

<style>
  .move-container {
    animation: move 2.5s ease-in-out infinite;
  }

  @keyframes move {
    0%,
    100% {
      transform: translateY(0);
    }
    50% {
      transform: translateY(-9px);
    }
  }
  .move-from-buttom {
    animation: moveFromBottomRight4 1s ease-in-out;
  }

  @keyframes moveFromBottomRight4 {
    0% {
      transform: translate(00%, 0%);
      opacity: 0;
    }
    100% {
      transform: translate(0, 0);
      opacity: 1;
    }
  }
  .custom-scrollbar::-webkit-scrollbar {
    margin-top: 1rem;
    width: 2px;
    height: 0rem;
    background-color: black;
  }

  /* Style the scrollbar thumb */
  .custom-scrollbar::-webkit-scrollbar-thumb {
    background-color: #888;
    border-radius: 1px;
  }

  /* Style the scrollbar thumb when hovered */
  .custom-scrollbar::-webkit-scrollbar-thumb:hover {
    background-color: #555;
  }
</style>
