<!-- JS -->
<script>
import HeaderNavBar from './components/HeaderNavBar.vue'
import MainCards from './components/MainCards.vue'

export default {

  components: {
    HeaderNavBar,
    MainCards
},


}
</script>

<!-- HTML -->

<template>
  <HeaderNavBar />
  <MainCards />

</template>

<!-- CSS -->

<style lang="scss">
@use './style/general';

</style>