<template>
  <div id="app">
    <!-- header -->
    <header id="header">
      <div class="container">
        <div class="cart">
          <p><i class="fas fa-shopping-cart"></i> {{ cart.length }}</p>
        </div>
      </div>
    </header>

    <ProductDetail @addtocart="updatecart" :member="member"></ProductDetail>
  </div>
</template>

<script>
import ProductDetail from "./components/ProductDetail.vue";

export default {
  name: "App",
  components: {
    ProductDetail,
  },
  data() {
    return {
      member: true,
      cart: [],
    };
  },
  methods: {
    updatecart(id) {
      this.cart.push(id);
    },
  },
};
</script>
