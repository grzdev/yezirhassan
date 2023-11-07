<script>
  import WorkImg from "../image/workImg.jpeg";
</script>

<div
  class="flex flex-row gap-[3rem] p-[2rem] overflow-x-auto custom-scrollbar mt-[-1rem] move-container"
>
  <div class="flip-container mt-[2rem] move-from-buttom">
    <div class="flip-card">
      <div
        class="flip-front gap-[2rem] justify-center items-center flex flex-col bg-green-800 container"
      >
        <div>
          <img
            src={WorkImg}
            alt=""
            class="w-[14rem] sm:w-[20rem] md:w-[20rem] rounded-lg"
          />
        </div>
        <h1
          class="text-[1.4rem] sm:text-[2rem] md:text-[2rem] font-bold text-white"
        >
          Basketball Courts
        </h1>
        <div
          class="w-[6rem] sm:w-[8rem] md:w-[8rem] h-[2rem] sm:h-[2.5rem] md:h-[2.5rem] rounded-lg bg-[white] justify-center items-center flex"
        >
          <h1
            class="text-[1rem] sm:text-[1.2rem] md:text-[1.2rem] font-semibold text-black"
          >
            Basketball
          </h1>
        </div>
      </div>
      <div
        class="flip-back justify-center items-center flex flex-col gap-[1rem] sm:gap-[2rem] md:gap-[2rem] bg-green-800"
      >
        <div class="flex flex-row gap-[2rem]">
          <h1 class="text-[1rem] sm:text-[1.2rem] md:text-[1.2rem] font-medium">
            7 mins read
          </h1>
          <h1 class="text-[1rem] sm:text-[1.2rem] md:text-[1.2rem] font-medium">
            November 20
          </h1>
        </div>
        <p
          class="w-[16rem] sm:w-[18rem] md:w-[18rem] text-[1.1rem] font-medium"
        >
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Labore,
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Labore,
          Lorem ipsum dolor sit amet
        </p>
        <h1
          class="text-[1rem] sm:text-[1.2rem] md:text-[1.2rem] font-medium underline decoration-solid"
        >
          Read full article →
        </h1>
      </div>
    </div>
  </div>
</div>

<style>
  .container {
    width: 100%;
    height: 100%;
    /* Add your background pattern here */
    background-image: repeating-radial-gradient(
      #499a52 80%,
      #346939 90%,
      #499a52 90%
    );
    background-size: 65px 65px;
  }
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

  .move-from-buttom3 {
    animation: moveFromBottomRight3 1.3s ease-in-out;
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
    width: 23rem;
    height: 25rem;
    transition: transform 0.5s;
    transform-style: preserve-3d;
  }

  @media (max-width: 640px) {
    /* Set different width and height for smaller screens */
    .flip-card {
      width: 17rem;
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
</style>
