<!-- JS -->
<script>
import HeaderNavBar from './components/HeaderNavBar.vue'
import Cards from './components/Cards.vue'
import FooterAction from './components/FooterAction.vue'
import productsData from './Data/db.json'

export default {

  components: {
    HeaderNavBar,
    Cards,
    FooterAction,
  },

  data() {
    return {
      products: productsData.products
    }
  }

}
</script>

<!-- HTML -->

<template>
  <HeaderNavBar />
  <main>
    <div class="container product">
      <div class="row">
        <Cards :products="products"/>
      </div>
    </div>
  </main>

  <FooterAction />

</template>

<!-- CSS -->

<style lang="scss">
@use './style/general';
</style>