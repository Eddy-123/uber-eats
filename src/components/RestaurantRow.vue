<template>
    <div class="restaurant--row">
        <h2 class="title">Nos restaurants</h2>
        <div class="wrapper">
            <RestaurantCard v-for="(card, index) in 3" :key="index"/>
        </div>
    </div>
</template>

<script>
import RestaurantCard from './RestaurantCard.vue'

export default {
    name: 'RestaurantRow',
    components: {
        RestaurantCard,
    }
}
</script>

<style lang='scss'>
.restaurant--row{
    .title{
        font-size: 2rem;
    }
    .wrapper{
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
}
</style>