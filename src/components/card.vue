  
<script>
import products from '../data/products.js';
export default {
  name:'card',
  props:{
    product: 'object',

  },
  data(){
    return{
      products
    }
  }
}
</script>

<template>
  <div class="col">
    <!-- card  -->
    <div class="card">
      <div class="card-image">
        <div class="images">
          <img :src="`/img/`+product.primaryImage" :alt="product.primaryImage">
          <img class="secondary-image" :src="`/img/`+product.secondaryImage" :alt="product.secondaryImage">
        </div>
        <div class="favourite">&hearts;</div>
        <div class="card-badge">
          <span v-if="product.discount" class="badge discount">{{product.discount}}</span>
          <span v-if="product.sostenibilita" class="badge tag">Sostenibilità</span>
        </div>
      </div>
      <div class="card-text">
        <span class="brand">{{ product.marca }}</span>
        <h3 class="product-name">{{ product.modello }}</h3>
        <div class="price">
          <span>{{ product.lastPrice }}</span>
          <del>{{ product.fullPrice }}</del>
        </div>
      </div>
    </div> 
    <!-- /card  -->
  </div>
</template>

<style lang="scss" scoped>
@use '../scss/partials/variabiles' as *;


.card .card-image{
      position: relative;
      cursor: pointer;

      &:hover .secondary-image{
        display: block;
      }

      .secondary-image{
        position: absolute;
        top: 0;
        left: 0;
        display: none;
      }

      .favourite,
      .card-badge{
        position: absolute;
      }
      .favourite{
        top:10px;
        right: 0;
        background-color: white;
        padding: 20px 15px;
        font-size: 1.5rem;
        &:hover{
          color: $red;
        }
      }
      .card-badge{
        left: 0;
        bottom: 20px;
        color: white;
        font-weight: bold;

        .badge{
          padding: 5px 10px;
        }
        .discount{
          background-color: $red;
        }
        .tag{
          background-color:$bg-green;
          text-transform: capitalize;
        }
      }
    }
    .card .price{
      font-size: .9;

      span{
        color: $red;
        font-weight: bold;
        margin-right: 5px;
      }
    }

</style>