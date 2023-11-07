<script lang="ts">
  import WorkImg from "../image/workImg.jpeg";
  import type { Work } from "../components/workInterface";
  export let work: Work[] = [];
</script>

{#each work as work (work.id)}
  <div class="flip-container mt-[2rem] move-from-buttom">
    <div class="flip-card">
      <div
        class="flip-front gap-[1.7rem] sm:gap-[2rem] md:gap-[2rem] justify-center items-center flex flex-col bg-green-800 bg-gradient-to-r from-green-600 via-green-700 to-green-800"
      >
        <div>
          <img
            src={WorkImg}
            alt=""
            class="w-[13rem] sm:w-[17rem] md:w-[17rem] rounded-lg"
          />
        </div>
        <h1
          class="text-[1.2rem] sm:text-[1.7rem] md:text-[1.7rem] font-bold text-white w-[13rem] sm:w-[18rem] md:w-[18rem]"
        >
          <!-- Basketball Courts in Nigeria -->
          {work.topic}
        </h1>
        <div
          class="w-[6rem] sm:w-[7rem] md:w-[7rem] h-[2rem] sm:h-[2.5rem] md:h-[2.5rem] rounded-lg bg-[white] justify-center items-center flex"
        >
          <h1 class="text-[1rem] font-semibold text-black">
            {work.category}
          </h1>
        </div>
      </div>
      <div
        class="flip-back text-white justify-center items-center flex flex-col gap-[1rem] sm:gap-[2rem] md:gap-[2rem] bg-green-900"
      >
        <div class="flex flex-row gap-[1rem]">
          <h1 class="text-[1rem] sm:text-[1.2rem] md:text-[1.2rem] font-medium">
            {work.minread} read
          </h1>
          <h1 class="text-[1rem] sm:text-[1.2rem] md:text-[1.2rem] font-medium">
            {work.datePosted}
          </h1>
        </div>
        <p
          class="w-[13rem] sm:w-[18rem] md:w-[18rem] text-[1.1rem] font-medium"
        >
          {work.desc}
        </p>
        <a href={work.link}>
          <h1
            class="text-[1rem] sm:text-[1.2rem] md:text-[1.2rem] font-medium underline decoration-solid"
          >
            Read full article →
          </h1>
        </a>
      </div>
    </div>
  </div>
{/each}

<style>
  .move-from-buttom {
    animation: moveFromBottomRight4 0.5s ease-in-out;
  }

  @keyframes moveFromBottomRight4 {
    0% {
      transform: translate(10%, 20%);
      opacity: 0;
    }
    100% {
      transform: translate(0, 0);
      opacity: 1;
    }
  }

  .move-from-buttom2 {
    animation: moveFromBottomRight2 1s ease-in-out;
  }

  @keyframes moveFromBottomRight2 {
    0% {
      transform: translate(10%, 40%);
      opacity: 0;
    }
    100% {
      transform: translate(0, 0);
      opacity: 1;
    }
  }

  @keyframes moveFromBottomRight3 {
    0% {
      transform: translate(10%, 60%);
      opacity: 0;
    }
    100% {
      transform: translate(0, 0);
      opacity: 1;
    }
  }

  .flip-card {
    position: relative;
    width: 20rem;
    height: 25rem;
    transition: transform 0.5s;
    transform-style: preserve-3d;
  }

  @media (max-width: 640px) {
    /* Set different width and height for smaller screens */
    .flip-card {
      width: 15rem;
      height: 19rem;
    }
  }

  .flip-container:hover .flip-card {
    transform: rotateY(-180deg);
  }

  .flip-front,
  .flip-back {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
  }
  .flip-front {
    border-radius: 1rem;
    /* background-color: #1a2c50; */
  }

  .flip-back {
    transform: rotateY(180deg);
    /* background-color: #1a2c50; */
    border-radius: 1rem;
  }
</style>
