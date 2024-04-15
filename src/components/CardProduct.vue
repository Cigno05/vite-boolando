<!-- JS -->
<script>

export default {

    props: ['product'],
    data() {
        return {
        };
    },

}

</script>

<!-- HTML -->

<template>

    <div class="card">
        <div class="card-photo">
            <div class="card-overlay">
                <img :src="`/img/${product.frontImage}`" alt="">
                <div class="overlay">
                    <img :src="`/img/${product.backImage}`" alt="">
                </div>
            </div>
            <div class="card-heart">
                &hearts;
                <div class="overlay-heart">
                    &hearts;
                </div>
            </div>

            <ul class="card-badge">
                <li v-for="(badgeItem, i) in product.badges" :key="i" :class="`badge--${badgeItem.type}`">
                    {{ badgeItem.value }}
                </li>

            </ul>

        </div>

        <div class="card-description">
            <h6 class="brand">{{ product.brand }}</h6>
            <h3 class="product--name">{{ product.name }}</h3>
            <h5 class="product--price">{{ product.price }} &euro; <span class="price-old">{{ product.price
                    }} &euro;</span></h5>
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

.card-badge {

    display: flex;
    flex-direction: row;

}

.badge--discount {
    background: red;
    color: white;
    z-index: 5;
    padding: 5px 10px;
    margin-right: 5px;
    order: -1;
}

.badge--tag {
    background-color: green;
    color: white;
    z-index: 5;
    padding: 5px;
    left: 50px;
}

.product--price {
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

.card-overlay {

    .overlay {
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

    &:hover {
        .overlay {
            opacity: 1;
        }

    }
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
