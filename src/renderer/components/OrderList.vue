<template>
  <div>
      <order-item v-for="(order, index) in orders" :key="index" :order="order"></order-item>
  </div>
</template>

<script>
import OrderItem from './OrderList/OrderItem'
export default {
  data () {
    return {
      orders: []
    }
  },
  components: { OrderItem }
}
</script>
