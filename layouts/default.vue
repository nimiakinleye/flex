<template>
  <div class="max-width mx-auto">
    <AppHeader class="max-width"/>
    <Nuxt />
    <AppFooter />
  </div>
</template>


<script>
import AppHeader from '../components/AppHeader'
import AppFooter from '../components/AppFooter'
export default {
  components: {
    AppHeader,
    AppFooter
  }
}
</script>

<style>
html {
  font-family:
    'Raleway',
    sans-serif,
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.container {
  @apply mx-auto mt-24 px-3
}

.container {
  animation-name: dissolve;
  animation-duration: 700ms;
}

.page-header {
  @apply text-center font-semibold text-5xl my-6
}

input {
  @apply bg-gray-300 outline-none pl-3 h-10 text-sm w-full rounded-md
}

select {
  @apply bg-gray-300 outline-none pl-3 h-10 text-sm w-full rounded-md
}

.my-bg {
  background-color: #49BEB7;
}

@keyframes dissolve {
  0%{opacity: 0}
  100%{opacity: 100}
}

.max-width{
  max-width: 1500px;
}

</style>
