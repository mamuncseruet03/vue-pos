<template>
    <div>
        <div>{{ order.showable_id }}</div>
        <div>
            <order-food-item v-for="(food, index) in order.foods" v-bind:key="index" :food="food"></order-food-item>
        </div>
    </div>
</template>

<script>
import OrderFoodItem from './OrderItem/OrderFoodItem'

export default {
  props: [ 'order' ],
  components: { OrderFoodItem }
}
</script>
