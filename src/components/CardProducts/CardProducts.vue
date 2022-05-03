<template>
    <div class="vertical container-card ">
        <img :src="card.src" alt="">
        <p>{{card.titleProducts}}</p>
    </div>
    
</template>

<script>
export default {
    name: 'CardProducts',
    props: {
       card : {
           type: Object
       }
    },

}
</script>

<style src="./style.scss" lang="scss" scoped />


