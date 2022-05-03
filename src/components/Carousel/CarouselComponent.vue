<template>
    <div class="app">
        <carousel >
            <carousel-slide v-for="slide in slides" :key="slide" class="carousel-slider">
                <img :src="slide.src" :alt="slide">
                <h3>{{slide.title_products}}</h3>
                <p>{{slide.value}}</p>
            </carousel-slide>
        </carousel>
    </div>    
</template>

<script>
import Carousel from './Carousel';
import CarouselSlide from './CarouselSlide';
export default {
   
    data(){
        return {
            slides: [
                {src: require('../../assets/images/card-calca.svg'),title_products: "Calça", value: 'R$ 240,00'},
                {src: require('../../assets/images/card-sapato.svg'), title_products: "Sapato", value: 'R$ 250,00'}, 
                {src: require('../../assets/images/card-camisa-simples.svg'), title_products: "Camisa Simples", value: 'R$ 260,00'},
                {src: require('../../assets/images/card-camisaSocial.svg'), title_products: "Camisa Social", value: 'R$ 270,00'},

            ]
        }
    },
    components : {
        Carousel : Carousel,
        CarouselSlide : CarouselSlide,
    }
}
</script>

<style lang="scss">

@import '@/assets/scss/index.scss';
    .app {
        display:flex;
        justify-content: center;
    }
    .carousel {
        
        position:relative;
        overflow: hidden;
        width: 310px;
        height:500px;

        
       

       
    }
    .btn {

       
        color:#FFF;
        height:50px;
        width:50px;
       
       
        
    }
    .btn:hover {
        cursor: pointer;
    }
    .btn:focus{
        outline:none;
    }
    .btn-next {
        top:50%;
        right:0;
        display: flex;
        align-items: center;
        justify-content: center;
        transform: rotate(180deg);
    }
    .btn-prev {
        top:50%;
        left:0;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .carousel-slider {
        position:absolute;
        top:0;
        left:0;
        bottom:0;
        right:0;

        p { 
        text-align: center;
       color: $primary-color;
        }

        h3 { 
            margin: 0;
                 text-align: center;
       color: $primary-color;
        }

     
    }
  
    .carousel-slider img {
        width:100%;
        height: 85%;
    }
</style>