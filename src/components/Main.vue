<script>
import products from '../data/products.js';
import card from './card.vue'
export default {
  name: 'Main',
  components: {
    card
  },
  data(){
    return{
      products
    }
  }
}
</script>

<template>
  <main>
    <div class="container">

      <div class="row d-flex flex-wrap">

         <card v-for="product in products" :key="product.id" :product="product"/>
         
          
      </div>

    </div>
   </main>
</template>

<style lang="scss" scoped>
  @use '../scss/partials/variabiles' as *;

main{
  padding-top: 130px;
  
  .row .col{
    width: calc(100% / 3);
    min-width: 250px;
    padding: 0 10px;
    margin-bottom: 20px;
    
  }
}
</style>