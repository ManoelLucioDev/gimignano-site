<template>
  <div class="home">
    <section class="horizontal">
      <img src="../../assets/images/italy.png" alt="image-italy" />

      <div class="content">
        <div id="subtitle">
          <p>Nossa</p>
          <p>Inspiração</p>
        </div>

        <p>{{ paragraph.inspirion }}</p>
      </div>
    </section>

    <section class="horizontal-reverse">
      <img src="../../assets/images/image-section.svg" alt="image-italy" />

      <div id="presentation" class="content">
        <p>{{ paragraph.presentation }}</p>
      </div>
    </section>

    <section id="products" class="vertical">
      <h2>Conheça nossos Produtos</h2>
      <div id="card-products" class="horizontal">
        <CardProducts v-for="card in cards" :key="card.id" :card="card" />
      </div>
    </section>

    <section id="coments">
      <div class="center content-coments">
        <h3>Depoimentos</h3>
        <div class="coments-spotlight">
          <p>jsdnkjvnjsbndjkskjdcjksndkcdnskj</p>
          <div class="horizontal">
            <h5>SobreNome,</h5>

            <h5>Nome</h5>
          </div>
        </div>
      </div>
      <div class="center container-spotlight">
        <div class="content-spotlight">
          <h3>Passe para o lado</h3>
          <Carousel />
        </div>
      </div>
    </section>

    <section id="photos">
      <div class="horizontal">
        <img v-for="image in images" :key="image" :src="image" alt="" />
      </div>
    </section>
  </div>
</template>

<script>
import CardProducts from "../../components/CardProducts/CardProducts.vue";
import Carousel from "../../components/Carousel/CarouselComponent.vue";

export default {
  name: "HomeView",
  components: {
    CardProducts,
    Carousel,
  },
  data() {
    return {
      paragraph: {
        inspirion:
          "A Gimignano é altamente inspirada pela Itália, homenageando a arte, a história e a cultura italiana",
        presentation:
          "Usar Gimignano deve fazer você se sentir bem. Designer altamente sofisticado, para voce se destacar em  todo o tipo de ambiente.",
      },
      cards: [
        {
          id: 1,
          src: require("../../assets/images/card-camisaSocial.svg"),
          titleProducts: "Camisa Social",
        },
        {
          id: 2,
          src: require("../../assets/images/card-sapato.svg"),
          titleProducts: "Sapato",
        },
        {
          id: 3,
          src: require("../../assets/images/card-camisa-simples.svg"),
          titleProducts: "Camisa Simples",
        },
        {
          id: 4,
          src: require("../../assets/images/card-calca.svg"),
          titleProducts: "Calça e Cinto",
        },
      ],
      images: [
        require("../../assets/images/image1.svg"),

        require("../../assets/images/image2.svg"),

        require("../../assets/images/image3.svg"),

        require("../../assets/images/image4.svg"),
      ],
    };
  },
};
</script>

<style src="./style.scss" lang="scss" scoped />
