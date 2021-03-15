<template>
  <div>
    <div class="container">
      <div>
        <div class="page-header">
          Why <span class="text-orange-500">Flex</span>
        </div>
        <div class="text-center md:px-32 mb-5">
          Budgeting for fun and relaxation is one of the hardest things to do
          for many people because of social and economic factors. With flex,
          working class and earners will find it very easy to plan and budget
          for fun things like shopping, holidays, vacation etc without worries
          and also find fun tourists attraction, events and more.
        </div>
        <div class="text-center my-12 font-semibold text-4xl">6 Ways To <span class="text-orange-500">Flex</span></div>
        <div class="flex flex-col-reverse lg:grid lg:grid-cols-2 lg:gap-x-12 lg:bg-gray-100 rounded-lg py-4 md:px-8 items-center">
          <div class="">
            <HowTo />
          </div>
          <div class="self-center"><img class="imgWidth" src="../assets/images/phone-mock.png" alt=""></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import HowTo from './HowTo'
export default {
  components: {
    HowTo
  }
}
</script>

<style>
.max-height{
  max-height: 45rem;
}
.imgWidth{
  width: 54rem;
}
</style>