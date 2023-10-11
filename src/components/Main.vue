<script>
import Card from './Card.vue'
import products from '../data/products'



export default {
  name : 'Main',

  data () {
    return {
      products
    }
  },

  components : {
    Card
  }
}
</script>

<template>
  <main>
    <div class="container flex clothes">

      <Card v-for="card in products" :cardObj="card" :key="card.id"/>
      
    </div>
  </main>
</template>

<style lang="scss" >

@use '../scss/partials/variabiles' as *;
.img {
  width: 100%;
  height: auto;
}

.clothes {
  flex-wrap: wrap;
  justify-content: space-between;
}

.product {
  position: relative;
  width: calc(100% / 3.1);
  margin-top: 100px;
  min-width: 260px;
}

.heart {
  position: absolute;
  top: 10px;
  right: 0;
  background-color: white;
  padding: 5px 10px;
}

.discount {
  position: absolute;
  bottom: 40px;
  left: 0;
  font-size: 10px;
  background-color: $RedDiscount;
  padding: 3px 10px;
  color: white;
  font-weight: bold;
}

.eco {
  position: absolute;
  bottom: 40px;
  left: 45px;
  font-size: 10px;
  background-color: $GreenEco;
  padding: 3px 10px;
  color: white;
  font-weight: bold;
}

.left {
  left: 0;
}

.brand {
  position: absolute;
  left: 0;
  bottom: -20px;
}

.item {
  position: absolute;
  left: 0;
  bottom: -40px;
}

.price {
  position: absolute;
  left: 0;
  bottom: -60px;
  color: $RedDiscount;
}

.old-price{
  position: absolute;
  left: 60px;
  bottom: -60px;
  text-decoration: line-through;
}

.imgb {
  width: 100%;
  position: absolute;
  top: 0;
  left: 0;
  display: none;
  .disappear:hover &{
    display: block;
    cursor: pointer;
  }
}

.rheart {
  position: absolute;
  top: 10px;
  right: 0;
  background-color: white;
  padding: 5px 10px;
  color: $RedDiscount;
  display: none;
  .disappearheart:hover &{
    display: block;
    cursor: pointer;
  }
}

</style>
