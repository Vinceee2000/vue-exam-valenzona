<template>
  <div id="app">
    <h1>Vue Exam Project</h1>
    <Products />
    <CartSummary :itemCount="5" />
  </div>
</template>

<script>
//part 1 
//answer "To create a Vue project, you need to install Node.js and npm first. 
// Then, install the Vue CLI globally using npm to scaffold and run your Vue application."
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
