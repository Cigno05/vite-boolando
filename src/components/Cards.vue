<!-- JS -->
<script>

export default {
    
    props: {
         products: Array,
         test: String,
    },
    data() {
        return {
        };
    },

    mounted() {
        console.log(this.products);
    }

}

</script>

<!-- HTML -->

<template>
    <div class="col-4" v-for="(productItem) in products">
        <div class="card">
            <div class="card-photo">
                <div class="card-overlay">
                    <img :src="`/img/${productItem.frontImage}`" alt="">
                    <div class="overlay">
                        <img :src="`/img/${productItem.backImage}`" alt="">
                    </div>
                </div>
               <div class="card-heart">
                    &hearts;
                    <div class="overlay-heart">
                        &hearts;
                    </div>
                </div>

                <div class="card-badge">
                    <span class="card-discount">
                        {{ ptoductItem.badges.type }}
                    </span>
                    <span class="card-eco">
                        {{ card.eco }}
                    </span>
                </div>

            </div>
           
            <div class="card-description">
                <h6 class="brand">{{ productItem.brand }}</h6>
                <h3 class="name-product">{{ productItem.name }}</h3>
                <h5 class="price-product">{{ (productItem.price) }} &euro; <span class="price-old">{{ productItem.price }} &euro;</span></h5>
            </div>
            
        </div>
    </div>
</template>

<!-- CSS -->

<style lang="scss" scoped>
.card {
    position: relative;

}

.product :is(.card-photo, .card-description) {
    padding: 10px;
}

.card-badge {
    position: absolute;
    padding: 0 12px;
    width: auto;
    height: auto;
    bottom: 100px;
    left: 0;
}

.card-heart {
    background: white;
    font-size: 25px;
    z-index: 5;
    position: absolute;
    top: 20px;
    right: 10px;
    padding: 5px 10px;

}

[class^="card-discount"] {
    background: red;
    color: white;
    z-index: 5;
    padding: 5px 10px;
    margin-right: 5px;
}

.card-eco {
    background-color: green;
    color: white;
    z-index: 5;
    padding: 5px;
    left: 50px;
}

.price-product {
    color: red;
    font-weight: bold;
}

.price-old {
    color: black;
    font-weight: lighter;
    text-decoration: line-through;
}

.card-overlay>img {
    display: block;
    position: relative;
}

/* OVERLAY */

.card-overlay .overlay {
    position: absolute;
    top: 0;
    left: 0;
    opacity: 0;
    padding: 10px;
    width: 100%;
    height: 100%;
    /* transition: ; */
    /* non mi fa selezionare opacity */

}

.card-overlay:hover .overlay {
    opacity: 1;

}

.card-heart {

    .overlay-heart {

        position: absolute;
        top: 5px;
        right: 10px;
        opacity: 0;
    }
}

.card-heart:hover .overlay-heart {
    opacity: 1;
    color: red;
}
</style>
