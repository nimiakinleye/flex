<template>
  <div class="container">
    <div class="page-header">
      Who We <span class="text-orange-500">Are</span>
    </div>
    <div class="md:grid md:grid-cols-2 gap-x-24">
      <div class="text-center">
        <div class="font-bold text-xl my-5">Our Mission</div>
        <div>
          To help people create and manage a work-life balance with inclusive
          financial management lifestyle
        </div>
      </div>
      <div class="text-center">
        <div class="font-bold text-xl my-5">Our Vision</div>
        <div>
          To create an all-round inclusive lifestyle for every hardworking
          person in respect to manage their financial life for fun and enjoyment
        </div>
      </div>
    </div>
    <div class="page-header">
      The Think <span class="text-orange-500">Tanks</span>
    </div>
    <div class="flex flex-wrap justify-between">
      <div class="flex flex-col items-center text-center mx-auto my-5">
        <div>
          <img
            class="rounded-full border-4 border-green-300 w-48"
            src="../assets/images/titi.jpg"
            alt=""
          />
        </div>
        <div class="font-semibold mt-1">Titilayo Sunday</div>
        <div class="flex flex-row justify-center items-center">
          <div class="font-light mr-1">Founder</div>
          <div
            :class="{ transform: titi, 'rotate-180': titi }"
            @click="titi = !titi"
          >
            <svg
              class="w-4 transition"
              fill="#000"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:svg="http://www.w3.org/2000/svg"
              enable-background="new 0 0 32 32"
              id="svg2"
              version="1.1"
              viewBox="0 0 32 32"
              xml:space="preserve"
            >
              <g id="background"><rect fill="none" height="32" width="32" /></g>
              <g id="arrow_x5F_down">
                <polygon points="2.002,10 16.001,24 30.002,10  " />
              </g>
            </svg>
          </div>
        </div>
        <div v-show="titi" class="text-white transition my-bg w-64 p-2 rounded">
          Founder of Flex. She is a self-taught product designer who thinks
          every hardworking person deserves to "chop life" no matter how small
          they earn. It started as a personal problem to her and then she
          decided to do something about it.
        </div>
      </div>
      <div class="flex flex-col items-center text-center mx-auto my-5">
        <div>
          <img
            class="rounded-full border-4 border-green-300 w-48"
            src="../assets/images/profile.jpg"
            alt=""
          />
        </div>
        <div class="font-semibold mt-1">Victor Adeyemi</div>
        <div class="flex flex-row justify-center items-center">
          <div class="font-light mr-1">Co-Founder</div>
          <div
            :class="{ transform: victor, 'rotate-180': victor }"
            @click="victor = !victor"
          >
            <svg
              class="w-4 transition"
              fill="#000"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:svg="http://www.w3.org/2000/svg"
              enable-background="new 0 0 32 32"
              id="svg2"
              version="1.1"
              viewBox="0 0 32 32"
              xml:space="preserve"
            >
              <g id="background"><rect fill="none" height="32" width="32" /></g>
              <g id="arrow_x5F_down">
                <polygon points="2.002,10 16.001,24 30.002,10  " />
              </g>
            </svg>
          </div>
        </div>
        <div
          v-show="victor"
          class="text-white transition my-bg w-64 p-2 rounded"
        >
          Undefined
        </div>
      </div>
      <div class="flex flex-col items-center text-center mx-auto my-5">
        <div>
          <img
            class="rounded-full border-4 border-green-300 w-48"
            src="../assets/images/salako.jpg"
            alt=""
          />
        </div>
        <div class="font-semibold mt-1">Salako Oluwaseun</div>
        <div class="flex flex-row justify-center items-center">
          <div class="font-light mr-1">CTO</div>
          <div
            :class="{ transform: seun, 'rotate-180': seun }"
            @click="seun = !seun"
          >
            <svg
              class="w-4 transition"
              fill="#000"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:svg="http://www.w3.org/2000/svg"
              enable-background="new 0 0 32 32"
              id="svg2"
              version="1.1"
              viewBox="0 0 32 32"
              xml:space="preserve"
            >
              <g id="background"><rect fill="none" height="32" width="32" /></g>
              <g id="arrow_x5F_down">
                <polygon points="2.002,10 16.001,24 30.002,10  " />
              </g>
            </svg>
          </div>
        </div>
        <div v-show="seun" class="text-white transition my-bg w-64 p-2 rounded">
          Seun is a mobile app developer and a staunch believer of "problem no
          dey finish" and that everyone deserves to flex their lifestyle.
        </div>
      </div>
      <div class="flex flex-col items-center text-center mx-auto my-5">
        <div>
          <img
            class="rounded-full border-4 border-green-300 w-48"
            src="../assets/images/shina.jpg"
            alt=""
          />
        </div>
        <div class="font-semibold mt-1">Owolabi Samuel</div>
        <div class="flex flex-row justify-center items-center">
          <div class="font-light mr-1">Founder</div>
          <div
            :class="{ transform: samuel, 'rotate-180': samuel }"
            @click="samuel = !samuel"
          >
            <svg
              class="w-4 transition"
              fill="#000"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:svg="http://www.w3.org/2000/svg"
              enable-background="new 0 0 32 32"
              id="svg2"
              version="1.1"
              viewBox="0 0 32 32"
              xml:space="preserve"
            >
              <g id="background"><rect fill="none" height="32" width="32" /></g>
              <g id="arrow_x5F_down">
                <polygon points="2.002,10 16.001,24 30.002,10  " />
              </g>
            </svg>
          </div>
        </div>
        <div
          v-show="samuel"
          class="text-white transition my-bg w-64 p-2 rounded"
        >
          Co founder of flex. A well skilled product Engineer with over 5 years
          of experience in different tech sector believes in the school of
          thought of all work and no flex makes life boring. Samuel believes
          everyone needs to FLEX and enjoy life no matter how little they earn.
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      titi: false,
      seun: false,
      samuel: false,
      victor: false,
    }
  },
}
</script>

<style>
</style>