<template>
  <div>
    <h2>Products List</h2>
    <ul>
      <li
        v-for="product in products"
        :key="product.name"
        :class="product.price >= 1000 ? 'expensive' : 'affordable'"
      >
        {{ product.name }}
        <span v-if="showPrices"> - {{ formatCurrency(product.price) }}</span>
      </li>
    </ul>
    <p><strong>Total Price:</strong> {{ formatCurrency(totalPrice) }}</p>
  </div>
</template>

<script>
import { formatCurrency } from '../helpers.js';

export default {
  name: 'Products',
  data() {
    return {
      products: [
        { name: "Apple", price: 1.0 },
        { name: "Banana", price: 0.5 },
        { name: "Cherry", price: 2.0 },
        { name: "Luxury Watch", price: 1500 },
      ],
      showPrices: true,
    };
  },
  computed: {
    totalPrice() {
      return this.products.reduce((sum, product) => sum + product.price, 0);
    }
  },
  methods: {
    formatCurrency,
  }
}
</script>

<style scoped>
.expensive {
  color: red;
  font-weight: bold;
}

.affordable {
  color: green;
}
</style>
