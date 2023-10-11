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
        <div class="col">

         <card />
         <card />
         <card />
         <card />
         <card />
         <card />
         
          
        </div>
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
  }
}
</style>