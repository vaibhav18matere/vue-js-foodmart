<template>
     <div class="card">
          <div class="card-title">{{ product.name }}</div>
          <div class="card-body">
               <ProductIcon :product="product"/>
               <form>
                    <div class="row">
                         <div class="cell">
                              <label>Type:</label>
                         </div>
                         <div class="cell">
                              <em>{{ product.type }}</em>
                         </div>
                    </div>
                    <div class="row">
                         <div class="cell">
                              <label>Price:</label>
                         </div>
                         <div class="cell">₹ {{ product.price.INR }}</div>
                    </div>
                    <div class="row">
                         <div class="cell">
                              <label>Quantity:</label>
                         </div>
                         <div class="cell">
                              <input type="number" v-model.number="quantity" />
                         </div>
                    </div>
               </form>
          </div>
          <div class="card-footer">
               <button @click="addToCart(product.name, quantity)" class="btn btn-light">
                    Add to cart
               </button>
          </div>
     </div>
</template>

<script>
import ProductIcon from './ProductIcon.vue'
export default {
  components: { ProductIcon },
  props: ['product', 'index', 'addToCart'],
  data () {
    return {
      quantity: 0
    }
  }
}
</script>
