<script>
export default {
  name: 'Header'
}
</script>

<template>
  <header>
    <div class="container d-flex justify-content-beetween align-center h-100">
      <nav class="main-menu">
        <ul class="d-flex">
          <li><a href="#">uomo</a></li>
          <li><a href="#">donna</a></li>
          <li><a href="#">bambino</a></li>
        </ul>
      </nav>

      <div class="box-logo">
        <div class="logo">
          <img src="img/boolean-logo.png" alt="Logo Boolean">
        </div>
      </div>
      
      <nav class="social-menu">
        <ul class="d-flex">
          <li><a href="#"><i class="fa-regular fa-user"></i></a></li>
          <li><a href="#"><i class="fa-regular fa-heart"></i></a></li>
          <li><a href="#"><i class="fa-solid fa-bag-shopping"></i></a></li>
        </ul>
      </nav>
    </div>
   </header>
</template>

<style lang="scss" scoped>

@use '../scss/partials/variabiles' as *;

header{
  position: fixed;
  left: 0;
  right: 0; /* al posto di dare with:100% */
  background-color: $bg-header;
  height: 80px;
  color: white;
  box-shadow: 0 1px 3px grey;
  z-index: 999;

  .container{
    padding: 0 10px;
    nav{
      width: 30%;
    }
    nav ul{
      list-style: none;
    }
    nav ul a{
      color: white;
      text-decoration: none;
      font-weight: bold;
      text-transform: capitalize;
      &:hover{
        text-decoration: underline;
      }
    }
    .main-menu a{
      padding-right: 20px;
    }
    .social-menu a{
      padding-left: 5px;
    }
    .social-menu ul{
      justify-content: flex-end;
    }
    .logo{
      width: 165px;
    }
  }
}

</style>