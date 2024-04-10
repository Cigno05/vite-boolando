<!-- JS -->
<script>
import HeaderNavBar from './components/HeaderNavBar.vue'
import MainCards from './components/MainCards.vue'
import FooterAction from './components/FooterAction.vue'

export default {

  components: {
    HeaderNavBar,
    MainCards,
    FooterAction
},


}
</script>

<!-- HTML -->

<template>
  <HeaderNavBar />
  <MainCards />
  <FooterAction />

</template>

<!-- CSS -->

<style lang="scss">
@use './style/general';

</style>