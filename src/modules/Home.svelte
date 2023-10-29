<script>
  import Icon from "@iconify/svelte";
</script>

<div class="flex flex-col jusitfy-center items-center p-[2rem]">
  <div class="grid grid-cols-2 mt-[1.5rem] sm:mt-[2rem] md:mt-[3rem]">
    <div class="">
      <h1
        class="text-[1.7rem] sm:text-[2rem] md:text-[2.5rem] font-semibold col-start-1 text-black dark:text-[#d1d1d1]"
      >
        Yezir Hassan,
      </h1>
    </div>
    <div class="col-span-2 ...">
      <h1
        class="text-[5rem] sm:text-[7rem] md:text-[9rem] font-bold text-black dark:text-[#d1d1d1] leading-[6rem] sm:leading-[7rem] md:leading-[14rem] mt-[1rem] sm:mt-[1rem] md:mt-[-1rem]"
      >
        Sports Journalist
      </h1>
    </div>
    <div class="col-start-2 ...">
      <h1
        class="text-lg sm:text-2xl md:text-3xl font-semibold text-black dark:text-[#d1d1d1] mt-[2rem] sm:mt-[2.5rem] md:mt-[1rem]"
      >
        and Web Developer.
      </h1>
    </div>
  </div>
  <div
    class="flex flex-row items-center justify-center mt-[5rem] sm:mt-[7rem] md:mt-[7rem]"
  >
    <button
      class="text-black dark:text-[#d1d1d1] hover:text-black dark:hover:text-white flex flex-row items-center text-[1.5rem] sm:text-[1.5rem] md:text-[2rem]"
    >
      Explore
      <Icon
        icon="ic:sharp-arrow-outward"
        class="ml-[0.4rem] text-[1.5rem] sm:text-[1.8rem] md:text-[2.4rem]"
      />
    </button>
  </div>
</div>

<style>
  button {
    font-family: inherit;
    font-weight: 700;
    cursor: pointer;
    position: relative;
    border: none;
    background: none;
    transition-timing-function: cubic-bezier(0.25, 0.8, 0.25, 1);
    transition-duration: 400ms;
    transition-property: color;
  }

  button:focus,
  /* button:hover {
    color: rgb(170, 170, 170);
  } */

  button:focus:after,
  button:hover:after {
    width: 100%;
    left: 0%;
  }

  button:after {
    content: "";
    pointer-events: none;
    bottom: -2px;
    left: 50%;
    position: absolute;
    width: 0%;
    height: 2px;
    background-color: rgb(114, 114, 114);
    transition-timing-function: cubic-bezier(0.25, 0.8, 0.25, 1);
    transition-duration: 400ms;
    transition-property: width, left;
  }
</style>
