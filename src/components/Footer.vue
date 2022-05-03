<template>
  <div class="container">
    <div class="center footer">
      <p>Criado por Twofriends Technology</p>
    </div>
   <a href="https://web.whatsapp.com/send?phone=558197722813" target="_blank"><img src="../assets/images/whats.png" alt="whatssap" /></a> 
  </div>
</template>

<script>
export default {
  name: "FooterComponent",
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/index.scss";

.container {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: $primary-color;
  width: 100%;
  margin-top: 75px;
  img {
    background-color: $primary-color;
    margin-right: 40px;
    height: 30px;
    width: 30px;
  }
}

.footer {
  height: 80px;
  background-color: $primary-color;
  color: #fff;
  width: 100%;
}
</style>
