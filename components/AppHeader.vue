<template>
  <div class="fixed z-20 top-0 w-full">
    <div class="bg-white flex flex-row items-center justify-between lg:grid lg:grid-cols-12 px-3 lg:px-12 shadow-lg font-semibold">
      <nuxt-link to="/">
        <Logo class="w-24"/>
      </nuxt-link>
      <div class="nav-links hidden lg:flex items-center justify-self-end col-start-2 col-end-13">
        <nuxt-link class="ml-10 hover:text-orange-500 hover:bg-gray-100 px-2 py-1 rounded" to="why">
          Flex
        </nuxt-link>
        <nuxt-link class="ml-10 hover:text-orange-500 hover:bg-gray-100 px-2 py-1 rounded" to="who-we-are">
          Who we are
        </nuxt-link>
        <nuxt-link class="ml-10 hover:text-orange-500 hover:bg-gray-100 px-2 py-1 rounded" to="/partner">
          Become a partner
        </nuxt-link>
        <nuxt-link class="ml-10 hover:text-orange-500 hover:bg-gray-100 px-2 py-1 rounded" to="/faqs">
          FAQs
        </nuxt-link>
        <nuxt-link class="ml-10 bg-orange-500 hover:bg-orange-600 px-3 py-1 text-white rounded" to="join">
          Join Our Flex List
        </nuxt-link>
      </div>

      <div
      class="inset-x-0 transition lg:hidden"
      >
        <div
          class="ring-1 ring-black ring-opacity-5 divide-y-2 divide-gray-50 navSwipe"
        >
          <div class="">
            <div class="">
              <button
                type="button"
                class="bg-white rounded-b-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500"
                @click="toggleNav"
              >
                <span class="sr-only">Close menu</span>
                <!-- Heroicon name: outline/x -->
                <div v-html="navSVG"></div>
              </button>
            </div>
          </div>
        </div>
      </div>

    </div>
    <div v-show="navShow" class="py-6 z-20 animate-slide rounded-lg shadow-lg ring-1 ring-black ring-opacity-5 bg-white divide-y-2 divide-gray-50 navSwipe">
      <nav class="justify-items-center grid grid-cols-1 gap-y-6">
        <nuxt-link
          to="/why"
          class="text-base font-medium text-gray-900 hover:text-gray-700"
        >
          Flex
        </nuxt-link>
        <nuxt-link
          to="/who-we-are"
          class="text-base font-medium text-gray-900 hover:text-gray-700"
        >
          Who We Are
        </nuxt-link>
        <nuxt-link
          to="/partner"
          class="text-base font-medium text-gray-900 hover:text-gray-700"
        >
          Become a Partner
        </nuxt-link>
        <nuxt-link
          to="/faqs"
          class="text-base font-medium text-gray-900 hover:text-gray-700"
        >
          FAQs
        </nuxt-link>
        <nuxt-link
          to="/join"
          class="px-4 py-2 border border-transparent rounded-md shadow-sm text-base font-medium text-white bg-orange-500 hover:bg-orange-600"
        >
          Join Our Flex List
        </nuxt-link>
      </nav>
    </div>
  </div>
</template>

<script>
import Logo from './Logo'
export default {
  components: {
    Logo
  },
  data () {
    return {
      burger:  `<svg
                  class="h-6 w-6"
                  xmlns="http://www.w3.org/2000/svg"
                  fill="currentColor" 
                  width="24" height="24" 
                  viewBox="0 0 24 24"
                >
                  <path 
                    d="M24 
                    6h-24v-4h24v4zm0 
                    4h-24v4h24v-4zm0 
                    8h-24v4h24v-4z"
                  />
                </svg>`,
      close: `<svg
                  class="h-6 w-6"
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                  aria-hidden="true"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M6 18L18 6M6 6l12 12"
                  />
                </svg>`,
      navSVG: `<svg
                  class="h-6 w-6"
                  xmlns="http://www.w3.org/2000/svg"
                  fill="currentColor" 
                  width="24" height="24" 
                  viewBox="0 0 24 24"
                >
                  <path 
                    d="M24 
                    6h-24v-4h24v4zm0 
                    4h-24v4h24v-4zm0 
                    8h-24v4h24v-4z"
                  />
                </svg>`,
      navShow: false,
      subMenu: false,      
    }
  },
  methods: {
    toggleNav(){
      if(this.navSVG != this.close) {
        this.navSVG = this.close;
        this.navShow = true
      } else {this.navSVG = this.burger; this.navShow = false}
    }
  }
}
</script>

<style>
.nav-links .nuxt-link-exact-active {
  background-color: #49BEB7;
  color: white;
}
@keyframes slideDown {
  0% {
    transform: translateY(-200%);
  }
  100% {
    transform: none;
  }
}
  .animate-slide {
  animation-fill-mode: both;
  animation-duration: 1000ms;
  animation-iteration-count: 1;
  opacity: 1;
  animation-name: slideDown;
}
</style>