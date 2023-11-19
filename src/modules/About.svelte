<script>
  import { fade } from "svelte/transition";
  import Yezir from "../image/yezir.png";
</script>

<div class="flex flex-col justify-center items-center">
  <div
    class="flex flex-col sm:flex-col md:flex-row justify-center items-center mt-[2rem] sm:mt-[3rem] md:mt-[2rem]"
  >
    <div
      class="hidden md:block w-[22rem] sm:w-[32rem] md:w-[32rem] mt-[1rem] sm:mt-[1rem] md:mt-[3rem]"
    >
      <h1
        class="text-center sm:text-start md:text-start text-fade text-xl sm:text-2xl md:text-2xl hover:text-black dark:hover:text-white transition duration-500 ease-in-out text-[#6a6868] dark:text-[#989898] font-semibold"
      >
        Hey there! 👋🏽
      </h1>
      <div>
        <h1
          class="text-center sm:text-start md:text-start text-animation text-3xl sm:text-5xl md:text-5xl mt-[1rem] leading-[2rem] sm:leading-[4rem] md:leading-[4rem] font-bold hover:text-black dark:hover:text-white transition duration-500 ease-in-out text-[#424141] dark:text-[#bbbaba]"
        >
          Sports Journalist,
        </h1>
        <h1
          class="text-center sm:text-start md:text-start text-animation2 text-3xl sm:text-5xl md:text-5xl mt-[1rem] leading-[2rem] sm:leading-[4rem] md:leading-[4rem] font-bold hover:text-black dark:hover:text-white transition duration-500 ease-in-out text-[#424141] dark:text-[#bbbaba]"
        >
          Backend developer &
        </h1>
        <h1
          class="text-center sm:text-start md:text-start text-animation3 text-3xl sm:text-5xl md:text-5xl mt-[1rem] leading-[2rem] sm:leading-[4rem] md:leading-[4rem] font-bold hover:text-black dark:hover:text-white transition duration-500 ease-in-out text-[#424141] dark:text-[#bbbaba]"
        >
          Creative Manager
        </h1>
      </div>
    </div>
    <div class="">
      <img
        src={Yezir}
        alt=""
        class="text-fade mt-[0] sm:mt-[0] md:mt-[] w-[20rem] sm:w-[26rem] md:w-[28rem]"
      />
      <h1
        class="block md:hidden text-center mt-[1rem] text-fade text-2xl hover:text-black dark:hover:text-white transition duration-500 ease-in-out text-[#6a6868] dark:text-[#989898] font-semibold"
      >
        Hey there 👋🏽
      </h1>
    </div>
  </div>

  <div
    class="w-full h-[45rem] sm:h-[35rem] md:h-[35rem] bg-[#bdbdbd] dark:bg-[#19191A] mt-[5rem] md:mt-[8rem] flex justify-center items-center flex-col gap-[3rem]"
  >
    <p
      class="hidden md:block text-left w-[20rem] sm:w-[40rem] md:w-[50rem] text-xl sm:text-xl md:text-2xl font-bold leading-[2.5rem] sm:leading-[2.5rem] md:leading-[2.7rem] text-[#2b2b2b] dark:text-[#eceaea]"
    >
      Sports journalist with a Mass Communication degree, blending my passion
      for sports with my proficiency in Python to craft compelling narratives
      enriched with data and statistics. Transforming games into stories through
      the lens of analytics.
    </p>
    <p
      class="block md:hidden text-left w-[20rem] sm:w-[40rem] md:w-[50rem] text-xl sm:text-xl md:text-xl font-bold leading-[2.5rem] sm:leading-[2.5rem] md:leading-[2.7rem] text-[#2b2b2b] dark:text-[#eceaea]"
    >
      Sports journalist with a Mass Communication degree, blending my passion
      for sports with my proficiency in Python to craft compelling narratives
      enriched with data and statistics.
    </p>
    <p
      class="block md:hidden text-left w-[20rem] sm:w-[40rem] md:w-[50rem] text-xl sm:text-xl md:text-xl font-bold leading-[2.5rem] sm:leading-[2.5rem] md:leading-[2.7rem] text-[#2b2b2b] dark:text-[#eceaea]"
    >
      Transforming games into stories through the lens of analytics.
    </p>
    <p
      class="text-left w-[20rem] sm:w-[40rem] md:w-[50rem] text-xl sm:text-xl md:text-2xl font-bold leading-[2.5rem] sm:leading-[2.5rem] md:leading-[2.7rem] text-[#2b2b2b] dark:text-[#eceaea]"
    >
      Beyond the field, I indulge in video games, appreciate art, and enjoy a
      lively kickabout in the park.
    </p>
  </div>

  <div class="w-full h-[10rem]" />
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
