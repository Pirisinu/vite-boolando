  
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
  <div class="card" v-for="card in products" :key="card.id">
    <div class="card-image">
      <div class="images">
        <img :src="`/img/`+card.primaryImage" :alt="card.primaryImage">
        <img :class="secondary-image" :src="card.secondaryImage" :alt="card.marca">
      </div>
      <div class="favourite">&hearts;</div>
      <div class="card-badge">
        <span v-if="card.discount" class="badge discount">{{card.discount}}</span>
        <span v-if="card.sostenibilita" class="badge tag">Sostenibilità</span>
      </div>
    </div>
    <div class="card-text">
      <span class="brand">{{ card.marca }}</span>
      <h3 class="product-name">{{ card.modello }}</h3>
      <div class="price">
        <span>{{ card.lastPrice }}</span>
        <del>{{ card.fullPrice }}</del>
      </div>
    </div>
  </div> 
  <!-- /card  -->
</template>

<style lang="scss" >

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