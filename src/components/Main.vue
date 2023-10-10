<script>
export default {
  name : 'Main'
}
</script>

<template>
  <main>
    <div class="container flex clothes">

      <div class="product">
        <div class="disappear">
          <img src="../assets/img/1.webp" alt="Relaxed Tee" title="Relaxed Tee" class="img">
          <img src="../assets/img/1b.webp" alt="Relaxed TeeB" title="Relaxed TeeB" class="imgb">
          <div class="disappearheart">
            <span class="heart"> &hearts; </span>
            <span class="rheart"> &hearts; </span>
          </div>
          <span class="discount"> -50% </span>
          <span class="eco">Sostenibilità</span>
        </div>
        
        
        <span class="brand">Levi's</span>
        <h3 class="item"> RELAXED FIT TEE UNISEX</h3>
        <span class="price"> 14,99 &euro;</span>
        <span class="old-price"> 29,99 &euro;</span>
      </div>

      <div class="product">
        <div class="disappear">
          <img src="../assets/img/2.webp" alt="Roses Tee" title="Roses Tee" class="img">
          <img src="../assets/img/2b.webp" alt="Roses TeeB" title="Roses TeeB" class="imgb">
          <div class="disappearheart">
            <span class="heart"> &hearts; </span>
            <span class="rheart"> &hearts; </span>
          </div>
          <span class="discount"> -30% </span>
          <span class="brand">Guess</span>
        </div>
        
        <h3 class="item"> ROSES TEE</h3>
        <span class="price"> 20,99 &euro;</span>
        <span class="old-price"> 29,99 &euro;</span>
      </div>

      <div class="product">
        <div class="disappear">
          <img src="../assets/img/3.webp" alt="Tailleur" title="Tailleur" class="img">
          <img src="../assets/img/3b.webp" alt="TailleurB" title="Tailleur" class="imgb">
          <div class="disappearheart">
            <span class="heart"> &hearts; </span>
            <span class="rheart"> &hearts; </span>
          </div>
          <span class="discount"> -30% </span>
        </div>
        
        <span class="brand">Come Zucchero Filato</span>
        <h3 class="item"> VOGLIA DI COLORI PASTELLO</h3>
        <span class="price"> 129,99 &euro;</span>
        <span class="old-price"> 184,99 &euro;</span>
      </div>

      <div class="product">
        <div class="disappear">
          <img src="../assets/img/4.webp" alt="Unisex Tee" title="Unisex Tee" class="img">
          <img src="../assets/img/4b.webp" alt="Unisex TeeB" title="Unisex TeeB" class="imgb">
          <div class="disappearheart">
            <span class="heart"> &hearts; </span>
            <span class="rheart"> &hearts; </span>
          </div>
          <span class="discount"> -50% </span>
          <span class="eco">Sostenibilità</span>
        </div>
        
        <span class="brand">Levi's</span>
        <h3 class="item">TEE UNISEX</h3>
        <span class="price"> 14,99 &euro;</span>
        <span class="old-price"> 29,99 &euro;</span>
      </div>

      <div class="product">
        <div class="disappear">
          <img src="../assets/img/5.webp" alt="Stripe Bodice" title="Stripe Bodice" class="img">
          <img src="../assets/img/5b.webp" alt="Stripe BodiceB" title="Stripe BodiceB" class="imgb">
          <div class="disappearheart">
            <span class="heart"> &hearts; </span>
            <span class="rheart"> &hearts; </span>
          </div>
        </div>
        <span class="brand">Maya Deluxe</span>
        <h3 class="item"> Stripe Bodice </h3>
        <span class="price"> 99,99 &euro;</span>
      </div>

      <div class="product">
        <div class="disappear">
          <img src="../assets/img/6.webp" alt="Maglione" title="Maglione" class="img">
          <img src="../assets/img/6b.webp" alt="MaglioneB" title="MaglioneB" class="imgb">
          <div class="disappearheart">
            <span class="heart"> &hearts; </span>
            <span class="rheart"> &hearts; </span>
          </div>
          <span class="eco left">Sostenibilità</span>
        </div>
        
        <span class="brand">Esprit</span>
        <h3 class="item"> Maglione - Black</h3>
        <span class="price"> 29,99 &euro;</span>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>

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
