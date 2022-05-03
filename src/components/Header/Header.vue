<template>
  <div class="vertical header">
    <div class="horizontal wrapper-menu">
      <div>
        <img id="logo" alt="logo" src="../../assets/images/logo.svg" />
      </div>
      <div>
        <nav>
          <router-link to="/">Home</router-link>
          <router-link to="/products">Catálogo</router-link>
          <router-link to="/about">Nossa História</router-link>
        </nav>
      </div>
    </div>

    <div class="horizontal-reverse cartShopping">
      <img src="../../assets/images/shopping-cart.svg" alt="shopping-cart " />
    </div>
  </div>
</template>

<script>



export default {
  name: "HeaderComp",

};
</script>

<style src="./style.scss" lang="scss" />
