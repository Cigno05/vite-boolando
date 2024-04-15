<script>
import CardProduct from './CardProduct.vue';
import { store } from '../stores/store.js';

export default {
    components: {
        CardProduct,
    },
    data() {
        return {
            store: store,
        }
    },
}
</script>

<template>
    <main>
        <div class="container product">
            <div class="row">
                <div v-for="element in store.products" :key="element.id" class="col-4">
                    <CardProduct :product="element" />
                </div>
            </div>
        </div>
    </main>
</template>



<style lang="scss" scoped>
</style>