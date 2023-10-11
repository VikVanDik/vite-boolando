  
<script>

export default {
  name: 'Card',

  props : {
    cardObj : Object
  },

  data (){
    return {

    }
  }
}
</script>
  

<template>



<div class="product">
  <div class="disappear">
    <img :src="`../assets/img/${cardObj.primaryImage}`" alt="Relaxed Tee" title="Relaxed Tee" class="img">
    <img src="../assets/img/1b.webp" alt="Relaxed TeeB" title="Relaxed TeeB" class="imgb">
    <div class="disappearheart">
      <span class="heart"> &hearts; </span>
      <span class="rheart"> &hearts; </span>
    </div>
    <span class="discount"> {{cardObj.discount}} </span>
    <span class="eco">Sostenibilità</span>
  </div>
  
  
  <span class="brand">{{ cardObj.marca }}</span>
  <h3 class="item">{{ cardObj.modello }}</h3>
  <span class="price"> 14,99 &euro;</span>
  <span class="old-price"> 29,99 &euro;</span>
</div>

</template>


<style>

</style>