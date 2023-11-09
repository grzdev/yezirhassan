<script>
  import Yezir from "../image/yezir.png";
</script>

<div class="flex flex-row justify-center items-center">
  <div
    class="flex flex-col sm:flex-col md:flex-row justify-center items-center mt-[2rem] sm:mt-[3rem] md:mt-[-2rem]"
  >
    <div
      class="w-[22rem] sm:w-[32rem] md:w-[32rem] mt-[1rem] sm:mt-[1rem] md:mt-[3rem]"
    >
      <h1
        class="text-fade text-xl sm:text-2xl md:text-2xl text-start hover:text-black dark:hover:text-white transition duration-500 ease-in-out text-[#6a6868] dark:text-[#989898] font-semibold"
      >
        Hey there! 👋🏽
      </h1>
      <div>
        <h1
          class="text-animation text-3xl sm:text-5xl md:text-5xl mt-[1rem] text-start leading-[3rem] sm:leading-[4rem] md:leading-[4rem] font-bold hover:text-black dark:hover:text-white transition duration-500 ease-in-out text-[#424141] dark:text-[#bbbaba]"
        >
          Sports Journalist,
        </h1>
        <h1
          class="text-animation2 text-3xl sm:text-5xl md:text-5xl mt-[1rem] text-start leading-[3rem] sm:leading-[4rem] md:leading-[4rem] font-bold hover:text-black dark:hover:text-white transition duration-500 ease-in-out text-[#424141] dark:text-[#bbbaba]"
        >
          Backend developer &
        </h1>
        <h1
          class="text-animation3 text-3xl sm:text-5xl md:text-5xl mt-[1rem] text-start leading-[3rem] sm:leading-[4rem] md:leading-[4rem] font-bold hover:text-black dark:hover:text-white transition duration-500 ease-in-out text-[#424141] dark:text-[#bbbaba]"
        >
          Creative Manager
        </h1>
      </div>
    </div>
    <img
      src={Yezir}
      alt=""
      class="text-fade mt-[2rem] sm:mt-[3rem] md:mt-[] w-[20rem] sm:w-[26rem] md:w-[28rem]"
    />
  </div>
</div>

<style>
  @keyframes fadeIn {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }
  .text-fade {
    /* display: inline-block; */
    animation: fadeIn 1.5s ease-in-out;
  }
  @keyframes fadeInUp {
    from {
      transform: translateY(100%);
      opacity: 0;
    }
    to {
      transform: translateY(0);
      opacity: 1;
    }
  }

  .text-animation {
    /* display: inline-block; */
    animation: fadeInUp 0.7s ease-in-out;
  }
  .text-animation2 {
    /* display: inline-block; */
    animation: fadeInUp 1s ease-in-out;
  }
  .text-animation3 {
    /* display: inline-block; */
    animation: fadeInUp 1.3s ease-in-out;
  }
</style>
