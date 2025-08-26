<template>
  <div>
    <p v-if="itemCount === 0">Cart is empty</p>
    <p v-else>Items in Cart: {{ itemCount }}</p>
  </div>
</template>

<script>
export default {
  name: "CartSummary",
  props: {
    itemCount: {
      type: Number,
      required: true
    }
  }
};
</script>
