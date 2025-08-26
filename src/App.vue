<template>
  <div id="app">
    <h1>Vue Exam Project</h1>
    <Products />
    <CartSummary :itemCount="5" />
  </div>
</template>

<script>
import Products from './components/Products.vue';
import CartSummary from './components/CartSummary.vue';

export default {
  name: 'App',
  components: {
    Products,
    CartSummary
  }
}
</script>
