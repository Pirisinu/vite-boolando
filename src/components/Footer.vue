<script>
export default {
  name: 'Footer'
}
</script>

<template>
  <footer>
    <div class="left-side">
      <h4>Boolando s.r.l</h4>
      <ul>
        <li><a href="#">Informazioni Legali</a></li>
        <li><a href="#">Informativa sula privacy</a></li>
        <li><a href="#">Diritto di recesso</a></li>
      </ul>
    </div>
    <div class="right-side">
      <h4>Trovaci anche su</h4>
      <ul>
        <li><i class="fa-brands fa-twitter"></i></li>
        <li><i class="fa-brands fa-facebook-f"></i></li>
        <li><i class="fa-brands fa-instagram"></i></li>
        <li><i class="fa-brands fa-pinterest-p"></i></li>
        <li><i class="fa-brands fa-youtube"></i></li>
      </ul>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use '../scss/partials/variabiles' as *;

footer{
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: $bg-footer;
  color: white;
  height: 100px;
  .left-side{
    h4{
      margin: 10px;
    }
    ul{
      display: flex;

      li{
        margin: 10px;
        &:hover{
          background-color: white;
          border-radius: 3px;
          scale: 1.1;
        }

        a{
          color: white;
          
          &:hover{
            color: $bg-header;
          }
        }
      }
    }
  }
  .right-side{
    margin-right: 40px;
    ul{
      margin-top: 20px;
      display: flex;
      justify-content: space-between;

      li{
        &:hover{
          border-radius: 3px;
          scale: 1.8;
        }
        i{
          &:hover{
            color: $bg-header;
          }
        }
      }
    }
  }
}
</style>