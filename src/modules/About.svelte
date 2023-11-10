<script>
  import Yezir from "../image/yezir.png";
</script>

<div class="flex flex-col justify-center items-center">
  <div
    class="flex flex-col sm:flex-col md:flex-row justify-center items-center mt-[2rem] sm:mt-[3rem] md:mt-[-2rem]"
  >
    <div
      class="w-[22rem] sm:w-[32rem] md:w-[32rem] mt-[1rem] sm:mt-[1rem] md:mt-[3rem]"
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
    <img
      src={Yezir}
      alt=""
      class="text-fade mt-[2rem] sm:mt-[3rem] md:mt-[] w-[20rem] sm:w-[26rem] md:w-[28rem]"
    />
  </div>

  <div
    class="w-full h-[115rem] sm:h-[65rem] md:h-[55rem] bg-[#bdbdbd] dark:bg-[#19191A] mt-[5rem] flex justify-center items-center flex-col gap-[3rem]"
  >
    <p
      class="text-left w-[20rem] sm:w-[40rem] md:w-[50rem] text-xl sm:text-xl md:text-xl font-semibold leading-[2.5rem] sm:leading-[2.5rem] md:leading-[2.7rem] text-[#2b2b2b] dark:text-[#eceaea]"
    >
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Labore, Lorem
      ipsum dolor sit amet, consectetur adipisicing elit. Labore,Lorem ipsum
      dolor sit amet, consectetur adipisicing elit. Labore, Lorem ipsum dolor
      sit amet, consectetur adipisicing elit. Labore, Lorem ipsum dolor sit
      amet, consectetur adipisicing elit. Labore,
    </p>
    <p
      class="text-left w-[20rem] sm:w-[40rem] md:w-[50rem] text-xl sm:text-xl md:text-xl font-semibold leading-[2.5rem] sm:leading-[2.5rem] md:leading-[2.7rem] text-[#2b2b2b] dark:text-[#eceaea]"
    >
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Labore, Lorem
      ipsum dolor sit amet, consectetur adipisicing elit. Labore,Lorem ipsum
      dolor sit amet, consectetur adipisicing elit. Labore, Lorem ipsum dolor
      sit amet, consectetur adipisicing elit. Labore,
    </p>
    <p
      class="text-left w-[20rem] sm:w-[40rem] md:w-[50rem] text-xl sm:text-xl md:text-xl font-semibold leading-[2.5rem] sm:leading-[2.5rem] md:leading-[2.7rem] text-[#2b2b2b] dark:text-[#eceaea]"
    >
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Labore, Lorem
      ipsum dolor sit amet, consectetur adipisicing elit. Labore,Lorem ipsum
      dolor sit amet, consectetur adipisicing elit. Labore, Lorem ipsum dolor
      sit amet, consectetur adipisicing elit. Labore,
    </p>
    <p
      class="text-left w-[20rem] sm:w-[40rem] md:w-[50rem] text-xl sm:text-xl md:text-xl font-semibold leading-[2.5rem] sm:leading-[2.5rem] md:leading-[2.7rem] text-[#2b2b2b] dark:text-[#eceaea]"
    >
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Labore, Lorem
      ipsum dolor sit amet, consectetur adipisicing elit. Labore,Lorem ipsum
      dolor sit amet, consectetur adipisicing elit. Labore, Lorem ipsum dolor
      sit amet, consectetur adipisicing elit. Labore,
    </p>
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
