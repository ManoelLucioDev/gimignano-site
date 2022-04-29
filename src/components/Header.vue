<template>
<div>
    <div class="header">
    <div>
      <img id=logo alt="logo" src="../assets/logo.svg">
    </div>
    <div>
      <nav>
        <router-link to="/">Home</router-link> 
        <router-link to="/products">Catálogo</router-link>
        <router-link to="/about">Nossa História</router-link>
      </nav>
      
    </div>

  </div>
  <img src="../assets/shopping-cart.svg" alt="shopping-cart">

</div>

</template>

<script>
export default {
  name: 
    'HeaderComp'
  
}
</script>

<style lang="scss">
$primary-color: #000D9C;
$hight-primary-color: #3543da;

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 70px;

nav {
  

  a {
    padding-right: 30px ;
    font-weight: bold;
    color: $primary-color;
    text-decoration: none;

  }
  a:hover {
      color: $hight-primary-color;
    }
}

}


</style>