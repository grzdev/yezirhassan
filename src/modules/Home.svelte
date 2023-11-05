<script>
  import Icon from "@iconify/svelte";
  import { fade } from "svelte/transition";
  import { onMount } from "svelte";

  const options = [
    "Sports Journalist.",
    "Creative Manager.",
    "Backend developer.",
  ];
  let currentIndex = 0;

  function changeOption() {
    // header text change
    const optionsElement = document.getElementById("options");
    if (optionsElement) {
      optionsElement.classList.add("fade-out");

      setTimeout(() => {
        optionsElement.textContent = options[currentIndex];
        optionsElement.classList.remove("fade-out");
      }, 500);

      currentIndex++;
      if (currentIndex >= options.length) {
        currentIndex = 0;
      }
    }
  }

  onMount(() => {
    // Trigger the changeOption function every 5 seconds
    setInterval(changeOption, 4000);
  });

  let fadeIn = false;
  onMount(() => {
    setTimeout(() => {
      fadeIn = true;
    }, 200);
  });
</script>

<div class="flex flex-col jusitfy-center items-center p-[2rem]">
  <!-- name/occupation -->
  <div class=" mt-[5.5rem] sm:mt-[2rem] md:mt-[3rem]">
    <div class="">
      <h2
        class="hover:text-black dark:hover:text-white transition duration-500 ease-in-out text-[3.5rem] sm:text-[7rem] md:text-[9rem] font-bold text-[#6a6868] dark:text-[#989898] leading-[4rem] sm:leading-[7rem] md:leading-[14rem] mt-[1rem] sm:mt-[3rem] md:mt-[1rem]"
      >
        <span id="options" class="">Sports Journalist.</span>
      </h2>
    </div>
  </div>

  <!-- Explore button -->
  <div
    class="flex flex-row items-center justify-center mt-[3rem] sm:mt-[6rem] md:mt-[4.5rem]"
  >
    <a href="/work">
      <button
        class=" duration-500 group cursor-pointer flex justify-center items-center font-extrabold"
      >
        <span> Explore</span>
      </button>
    </a>
  </div>

  <!-- Avatar -->
  {#if fadeIn}
    <div class="move-container">
      <h4 class="move-from-buttom">
        <Icon
          icon="emojione-monotone:newspaper"
          class=" text-4xl sm:text-5xl md:text-6xl text-[#2E9953] dark:text-[#52CC7C] absolute mt-[-21rem] ml-[-8rem] sm:mt-[-30rem] md:mt-[-28rem] sm:ml-[-14rem] md:ml-[-25rem]"
        />
      </h4>
      <h4 class="move-from-buttom">
        <Icon
          icon="fa6-solid:photo-film"
          class=" text-2xl sm:text-4xl md:text-4xl text-[#2E9953] dark:text-[#52CC7C] absolute mt-[-20rem] ml-[7rem] sm:mt-[-28rem] md:mt-[-26rem] sm:ml-[13rem] md:ml-[22rem]"
        />
      </h4>
      <h4 class="move-from-buttom">
        <Icon
          icon="fontisto:python"
          class=" text-3xl sm:text-4xl md:text-5xl text-[#2E9953] dark:text-[#52CC7C] absolute absolute mt-[4.3rem] ml-[-10rem] sm:mt-[-1rem] md:mt-[0.6rem] sm:ml-[-19rem] md:ml-[-28rem]"
        />
      </h4>
      <h4 class="move-from-buttom">
        <Icon
          icon="el:idea"
          class=" text-4xl sm:text-5xl md:text-6xl text-[#2E9953] dark:text-[#52CC7C] absolute mt-[4rem] ml-[8rem] sm:mt-[-1rem] md:mt-[0.1rem] sm:ml-[15rem] md:ml-[26rem]"
        />
      </h4>
    </div>
  {/if}
</div>

<style>
  @keyframes fadeIn {
    0% {
      opacity: 0; /* Start with opacity 0 */
    }
    100% {
      opacity: 1; /* End with opacity 1 (fully visible) */
    }
  }
  .move-container {
    animation: move 3s ease-in-out infinite;
  }

  @keyframes move {
    0%,
    100% {
      transform: translateY(0);
    }
    50% {
      transform: translateY(-15px);
    }
  }

  .move-from-buttom {
    animation: moveFromBottomRight4 1s ease-in-out;
  }

  @keyframes moveFromBottomRight4 {
    0% {
      transform: translate(30%, 60%);
      opacity: 0;
    }
    100% {
      transform: translate(0, 0);
      opacity: 1;
    }
  }
  button {
    padding: 0.1em 0.25em;
    width: 13em;
    height: 5.2em;
    background-color: #5c5c5c;
    border: 0.08em solid #fff;
    border-radius: 1rem 0 1rem 0;
    font-size: 12px;
  }

  button span {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    font-weight: 700;
    bottom: 0.4em;
    width: 8.25em;
    height: 3em;
    background: rgb(5, 51, 21);
    background: linear-gradient(
      304deg,
      rgba(5, 51, 21, 1) 0%,
      rgba(98, 199, 133, 1) 100%
    );

    border-radius: 0.8rem 0 0.8rem 0;
    font-size: 1.5em;
    color: #fff;
    border: 0.08em solid #fff;
    box-shadow: 0 0.4em 0.1em 0.019em #d3d1d1;
  }

  button span:hover {
    transition: all 0.5s;
    transform: translate(0, 0.4em);
    box-shadow: 0 0 0 0 #d3d1d1;
  }

  button span:not(hover) {
    transition: all 1s;
  }

  /* Name/Occupation */
  @keyframes moveFromBottomRight {
    0% {
      transform: translate(10%, 60%);
      opacity: 0;
    }
    100% {
      transform: translate(0, 0);
      opacity: 1;
    }
  }

  @keyframes moveFromBottomRight2 {
    0% {
      transform: translate(10%, 30%);
      opacity: 0;
    }
    100% {
      transform: translate(0, 0);
      opacity: 1;
    }
  }

  @keyframes moveFromBottomRight3 {
    0% {
      transform: translate(30%, 60%);
      opacity: 0;
    }
    100% {
      transform: translate(0, 0);
      opacity: 1;
    }
  }

  /* h1 {
    animation: moveFromBottomRight 1s ease-in-out;
  } */

  h2 {
    animation: moveFromBottomRight2 1s ease-in-out;
  }

  button {
    animation: moveFromBottomRight3 1s ease-in-out;
  }

  /* Icons */
</style>
