<script>
export default {
  name: 'Header'
}
</script>

<template>
  <header>
    <div class="container">
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

<style>
  header{
    position: fixed;
    width: 100%;
    background-color: #FA6903;
    height: 80px;
    color: white;
    box-shadow: 0 1px 3px grey;
    
    div{
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 100%;
    }
  }
</style>