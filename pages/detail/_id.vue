<template>
  <div>
    <div class="container">
      <div class="main-panel">
        <img
          class="product-image"
          :src="product.imageUrl"
          :alt="product.name"
        />
      </div>
      <div class="side-panel">
        <p class="name">name: {{ product.name }}</p>
        <p class="price">price: {{ product.price }}</p>
        <!-- <button type="button" @click="addToCart">Add to Cart</button> -->
      </div>
    </div>
  </div>
</template>

<script>
// import axios from 'axios';
import { fetchProductById } from '@/api/index';

export default {
  async asyncData({ params }) {
    // const id = console.log(params.id);
    const response = await fetchProductById(params.id);
    const product = response.data;
    return { product };
  },
  // created() {
  //   const id = console.log(this.$route.params.id);
  //   fetchProductById(id);
  // },
};
</script>

<style scoped>
.container {
  display: flex;
  margin: 2rem 0;
  justify-content: center;
}
.product-image {
  width: 500px;
  height: 375px;
}
.side-panel {
  display: flex;
  padding: 0 1rem;
  flex-direction: column;
  justify-content: center;
  width: 220px;
  text-align: center;
}
</style>
