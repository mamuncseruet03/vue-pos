<template>
  <div>
    <div>{{ food.name }}</div>
    <div>{{ food.price }}</div>
    <div>{{ food.quantity }}</div>
    <div>{{ food.quantity*food.price }}</div>
  </div>
</template>

<script>
export default {
  props: [ 'food' ]
}
</script>
