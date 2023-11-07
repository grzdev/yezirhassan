<script>
  import { fade } from "svelte/transition";
  import WorkCard from "../components/WorkCard.svelte";
</script>

<div class="">
  <h2
    class="move-from-buttom hover:text-black dark:hover:text-white transition duration-500 ease-in-out text-[2.8rem] sm:text-[4rem] md:text-[5rem] lg:text-[5rem] font-bold text-[#6a6868] dark:text-[#989898] mt-[1rem] sm:mt-[1rem] md:mt-[-3rem]"
  >
    Featured Work
  </h2>
  <div>
    <WorkCard />
  </div>
</div>

<style>
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
