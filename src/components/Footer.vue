<script>

import infos from '../data/infos'

export default {
  name : 'Footer',

  data (){
    return {
      infos
    }
  }
}
</script>

<template>
  <footer>
    <div class="container flex foot">
      <div class="left-foot">
        <h4>Boolando S.R.L.</h4>
        <ul>
          <li
          v-for ="(info, index) in infos"
          :key="index"><a :href="info.href">{{ info.text }}</a></li>
          
        </ul>
      </div>
  
      <div class="right-foot">
        <p class="search">Trovaci anche su</p>
        <ul class="flex">
          <li><a href="#"><i class="fa-brands fa-twitter"></i></a></li>
          <li><a href="#"><i class="fa-brands fa-square-facebook"></i></a></li>
          <li><a href="#"><i class="fa-brands fa-instagram"></i></a></li>
          <li><a href="#"><i class="fa-brands fa-pinterest"></i></a></li>
          <li><a href="#"><i class="fa-brands fa-youtube"></i></a></li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>

@use '../scss/partials/_general.scss' as *;

footer {
  background-color: black;
}

.foot {
  margin-top: 100px;
  justify-content: space-between;
  align-items: center;
  padding: 30px 0 30px;
}

.left-foot {
  color: white;
  h4 {
    font-size: .9rem;
    padding-bottom: 10px;
    padding-left: 5px;
  }
  ul {
    li{
      list-style: none;
      display: inline-block;
      a{
        font-size: .7rem;
        text-decoration: none;
        color: white;
        margin-right: 5px;
      }
    }
  }
}

.right-foot {
  color: white;
  height: 50px;
  ul{
    font-size: .8rem;
    li {
    padding-top: 10px;
    list-style: none;
    display: inline-block;
    a{
      text-decoration: none;
      color: white;
      margin-left: 5px;
    }
  }
  }
  
}

.search {
  font-size: .9rem;
  padding-top: 10px;
}

</style>
