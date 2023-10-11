  
<script>
import products from '../data/products.js';
export default {
  name:'card',
  data(){
    return{
      products
    }
  }
}
</script>

<template>
  <!-- card  -->
  <div class="card" >
    <div class="card-image">
      <div class="images">
        <img :src="`/img/`" :alt="products.primaryImage">
        <img class="secondary-image" src="product.secondaryImage" alt="nome prodotto...">
      </div>
      <div class="favourite">&hearts;</div>
      <div class="card-badge">
        <span class="badge discount">{{}}</span>
        <span v-if="true" class="badge tag">Sostenibilità</span>
      </div>
    </div>
    <div class="card-text">
      <span class="brand">{{  }}</span>
      <h3 class="product-name">{{ }}</h3>
      <div class="price">
        <span>{{  }}</span>
        <del>{{ }}</del>
      </div>
    </div>
  </div> 
  <!-- /card  -->
</template>

<style lang="scss" scoped>

  

</style>