<script>
export default {
  name: 'Main'
}
</script>

<template>
  <main>
    <div class="container">

      <div class="row d-flex flex-wrap">

        <!-- card  -->
        <div class="col ">
          <div class="card">
            <div class="card-image">
              <div class="images">
                <img src="../assets/img/1.webp" alt="nome prodotto...">
                <img class="secondary-image" src="../assets/img/1b.webp" alt="nome prodotto...">
              </div>
              <div class="favourite">&hearts;</div>
              <div class="card-badge">
                <span class="badge discount">-50%</span>
                <span class="badge tag">sostenibilità</span>
              </div>
            </div>
            <div class="card-text">
              <span class="brand">Levi's</span>
              <h3 class="product-name">RELAXED FIT TEE UNISEX</h3>
              <div class="price">
                <span>14,99 €</span>
                <del>29,99 €</del>
              </div>
            </div>
          </div> 
        </div>
        <!-- /card  -->

        <!-- card  -->
        <div class="col ">
          <div class="card">
            <div class="card-image">
              <div class="images">
                <img src="../assets/img/2.webp" alt="nome prodotto...">
                <img class="secondary-image" src="../assets/img/2b.webp" alt="nome prodotto...">
              </div>
              <div class="favourite">&hearts;</div>
              <div class="card-badge">
                <span class="badge discount">-50%</span>
                <span class="badge tag">sostenibilità</span>
              </div>
            </div>
            <div class="card-text">
              <span class="brand">Levi's</span>
              <h3 class="product-name">RELAXED FIT TEE UNISEX</h3>
              <div class="price">
                <span>14,99 €</span>
                <del>29,99 €</del>
              </div>
            </div>
          </div> 
        </div>
        <!-- /card  -->

        <!-- card  -->
        <div class="col ">
          <div class="card">
            <div class="card-image">
              <div class="images">
                <img src="../assets/img/3.webp" alt="nome prodotto...">
                <img class="secondary-image" src="../assets/img/3b.webp" alt="nome prodotto...">
              </div>
              <div class="favourite">&hearts;</div>
              <div class="card-badge">
                <span class="badge discount">-50%</span>
                <span class="badge tag">sostenibilità</span>
              </div>
            </div>
            <div class="card-text">
              <span class="brand">Levi's</span>
              <h3 class="product-name">RELAXED FIT TEE UNISEX</h3>
              <div class="price">
                <span>14,99 €</span>
                <del>29,99 €</del>
              </div>
            </div>
          </div> 
        </div>
        <!-- /card  -->

        <!-- card  -->
        <div class="col ">
          <div class="card">
            <div class="card-image">
              <div class="images">
                <img src="../assets/img/4.webp" alt="nome prodotto...">
                <img class="secondary-image" src="../assets/img/4b.webp" alt="nome prodotto...">
              </div>
              <div class="favourite">&hearts;</div>
              <div class="card-badge">
                <span class="badge discount">-50%</span>
                <span class="badge tag">sostenibilità</span>
              </div>
            </div>
            <div class="card-text">
              <span class="brand">Levi's</span>
              <h3 class="product-name">RELAXED FIT TEE UNISEX</h3>
              <div class="price">
                <span>14,99 €</span>
                <del>29,99 €</del>
              </div>
            </div>
          </div> 
        </div>
        <!-- /card  -->

        <!-- card  -->
        <div class="col ">
          <div class="card">
            <div class="card-image">
              <div class="images">
                <img src="../assets/img/5.webp" alt="nome prodotto...">
                <img class="secondary-image" src="../assets/img/5b.webp" alt="nome prodotto...">
              </div>
              <div class="favourite">&hearts;</div>
              <div class="card-badge">
                <span class="badge discount">-50%</span>
                <span class="badge tag">sostenibilità</span>
              </div>
            </div>
            <div class="card-text">
              <span class="brand">Levi's</span>
              <h3 class="product-name">RELAXED FIT TEE UNISEX</h3>
              <div class="price">
                <span>14,99 €</span>
                <del>29,99 €</del>
              </div>
            </div>
          </div> 
        </div>
        <!-- /card  -->

        <!-- card  -->
        <div class="col ">
          <div class="card">
            <div class="card-image">
              <div class="images">
                <img src="../assets/img/6.webp" alt="nome prodotto...">
                <img class="secondary-image" src="../assets/img/6b.webp" alt="nome prodotto...">
              </div>
              <div class="favourite">&hearts;</div>
              <div class="card-badge">
                <span class="badge discount">-50%</span>
                <span class="badge tag">sostenibilità</span>
              </div>
            </div>
            <div class="card-text">
              <span class="brand">Levi's</span>
              <h3 class="product-name">RELAXED FIT TEE UNISEX</h3>
              <div class="price">
                <span>14,99 €</span>
                <del>29,99 €</del>
              </div>
            </div>
          </div> 
        </div>
        <!-- /card  -->

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
          color: $bg-red;
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