<template>
     <div class="product-listing">
          <main class="wrapper">
               <h2>Available Products</h2>
               <div class="card-container">
                    <ProductCart v-for="(product, index) in inventory.slice(0, 9)" class="card" :key="product.id"
                         :index="index" :product="product" :addToCart="addToCart" />
               </div>
          </main>
     </div>
</template>

<script>
import ProductCart from '@/components/ProductCart.vue'
export default {
  props: ['inventory', 'addToCart'],
  components: {
    ProductCart
  }
}
</script>
