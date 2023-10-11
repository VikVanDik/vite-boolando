  
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
    <img :src="`/src/assets/img/${cardObj.primaryImage}`" alt="Relaxed Tee" title="Relaxed Tee" class="img">
    <img :src="`/src/assets/img/${cardObj.secondaryImage}`" alt="Relaxed TeeB" title="Relaxed TeeB" class="imgb">
    <div class="disappearheart">
      <span class="heart"> &hearts; </span>
      <span class="rheart"> &hearts; </span>
    </div>
    <span class="discount" v-if="cardObj.discount === null ? '' : 'd-none'"> {{cardObj.discount}} </span>
    <span class="eco" v-if="cardObj.sostenibilita === true ? '' : 'd-none'">Sostenibilità</span>
  </div>
  
  
  <span class="brand">{{ cardObj.marca }}</span>
  <h3 class="item">{{ cardObj.modello }}</h3>
  <span class="price"> {{ cardObj.lastPrice }} &euro;</span>
  <span class="old-price" v-if="cardObj.fullPrice === null ? '' : 'd-none'"> {{ cardObj.fullPrice }} &euro;</span>
</div>

</template>


<style>

</style>