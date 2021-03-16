<template>
  <div class="container">
    <div class="md:mt-32">
      <div class="flex flex-col-reverse md:px-3 md:flex-row items-center md:justify-between banner-height bg-hand-pattern bg-repeat rounded-3xl py-12">
        <div class="text-center md:text-left">
          <div class="font-semibold text-5xl">We Think You Should</div>
          <div class="font-semibold text-5xl text-orange-500 font-bold">FLEX</div>
          <div class="font-normal mb-5">
            Your No. 1 financial management tool to help you plan,
            <br />
            save and flex on your terms!
          </div>
          <div class="mb-5">
            <nuxt-link class="bg-orange-500 hover:bg-orange-600 px-3 py-1 text-white rounded" to="/join">
              Join Our Flex List
            </nuxt-link>
          </div>
          <div class="flex flex-row justify-between md:justify-start">
            <div class="bg-gray-900 mr-4 py-2 px-4 flex items-center text-white rounded-lg">
              <svg
                class="w-8 mr-4"
                viewBox="0 0 43 43"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M35.9514 22.7231C35.9285 19.1999 37.8249 16.5407 41.6634 14.5823C39.5157 12 36.2713 10.5792 31.9872 10.3008C27.9317 10.032 23.4992 12.2879 21.877 12.2879C20.1634 12.2879 16.2335 10.3968 13.149 10.3968C6.77444 10.4832 0 14.6687 0 23.1839C0 25.6991 0.548353 28.2975 1.64506 30.9791C3.10733 34.5023 8.38523 43.1422 13.8916 42.9982C16.7705 42.9406 18.8039 41.2798 22.551 41.2798C26.1838 41.2798 28.0688 42.9982 31.279 42.9982C36.831 42.931 41.6063 35.0783 43 31.5455C35.5515 28.5983 35.9514 22.9055 35.9514 22.7231ZM29.4854 6.95997C32.6041 3.84958 32.3185 1.0176 32.2272 0C29.474 0.134399 26.2867 1.57439 24.4702 3.35039C22.471 5.25118 21.2944 7.60317 21.5457 10.2528C24.5274 10.4448 27.2463 9.15836 29.4854 6.95997Z"
                  fill="white"
                />
              </svg>
              <div>
                <div>Will soon be on</div>
                <div class="font-semibold">App Store</div>
              </div>
            </div>
            <div class="bg-gray-900 py-2 px-4 flex items-center text-white rounded-lg">
              <svg
                class="w-8 mr-4"
                viewBox="0 0 37 45"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M24.0544 20.5968L6.35839 1.1428L28.8733 15.3135L24.0544 20.5968ZM1.73994 0C0.697578 0.597773 0 1.68783 0 3.10315V41.8969C0 43.3122 0.697578 44.4022 1.73994 45L22.3145 22.4956L1.73994 0ZM35.8331 19.832L31.1104 16.8343L25.8425 22.5044L31.1104 28.1744L35.9293 25.1768C37.3726 23.9197 37.3726 21.0891 35.8331 19.832ZM6.35839 43.866L28.8733 29.6953L24.0544 24.412L6.35839 43.866Z"
                  fill="white"
                />
              </svg>

              <div>
                <div>Will soon be on</div>
                <div class="font-semibold">Google Play</div>
              </div>
            </div>
          </div>
        </div>
        <div class="justify-self-center md:self-center img-width ">
          <!-- <img
            class="rounded-xl"
            src="../assets/images/flex.jpg"
            alt=""
          /> -->
          <div>
            <slide :data="slide" class="bg-gray-300 rounded-xl" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import slide from '@wyhaya/vue-slide'
export default {
  components: {
    slide
  },
  data () {
    return {
      slide: ['../images/flex.jpg']
    }
  }
}
</script>

<style>
@media (min-width : 767px) {
  .banner-height{
  max-height: 26rem;
  margin-top: 15rem;
  background-color: #49BEB7;
  background-image: url('../static/bg/hand.svg'),
                    url('../static/bg/hand.svg'),
                    url('../static/bg/hand.svg'),
                    url('../static/bg/hand.svg'),
                    url('../static/bg/hand.svg'),
                    url('../static/bg/hand.svg'),
                    url('../static/bg/hand.svg'),
                    url('../static/bg/hand.svg'),
                    url('../static/bg/hand.svg'),
                    url('../static/bg/hand.svg'),
                    url('../static/bg/hand.svg');
  background-repeat: no-repeat;
  background-position: 0 top,
                       300px top,
                       150px center,
                       600px top,
                       450px center,
                       900px top,
                       600px bottom,
                       750px center,
                       300px bottom,
                       900px bottom,
                       0 bottom;
}
}
.img-width{
  width: 25rem;
}
</style>