<!-- JS -->
<script>
import HeaderNavBar from './components/HeaderNavBar.vue'
import AppContent from './components/AppContent.vue'
import FooterAction from './components/FooterAction.vue'
import axios from 'axios'
import { store } from './stores/store.js'

export default {

  components: {
    HeaderNavBar,
    AppContent,
    FooterAction,
  },

  data() {
    return {

    }
  },
  methods: {
    fetchProducts() {
      axios.get('http://localhost:3000/products').then((res) => {
        // console.log(res) // risposta del server
        // console.log(res.data) // array dei prodotti
        store.products = res.data // salviamo l'arrai di prodotti dentro lo store
      })
    }
  },
  created() {
    this.fetchProducts()
  },
  mounted() {
    // axios.get('http://localhost:3000/products')
  }
}
</script>

<!-- HTML -->

<template>
  <HeaderNavBar />
  <AppContent />
  <FooterAction />


</template>

<!-- CSS -->

<style lang="scss">
@use './style/general';
</style>