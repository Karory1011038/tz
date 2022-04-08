<template>
      <HomePage/>
</template>

<script>
import HomePage from './components/HomePage.vue'

export default {
  name: 'App',

  components: {
    HomePage,
  },

  data: () => ({
    //
  }),
}
</script>
<style>
/*@import url("src/assets/fonts/mont/stylesheet.css");*/
.main-page {
  background: linear-gradient(239.67deg, #227164 0.34%, #278878 61.18%) ;
}
.full-screen {
  height: 100%; width: 100%;
}
</style>
