<script>

import units from '../data/units'
import icons from '../data/icons'

export default {
  name : 'Header',

  data () {
    return {
      units,
      icons
    }
  }
}
</script>

<template>
  <header>
    <div class="container flex head">
      <ul>
        <li 
        v-for = "(unit, index) in units"
        :key ="index"><a :href="unit.href">{{ unit.unitName }}</a></li>
      </ul>

      <img src="../assets/img/boolean-logo.png" alt="Logo" class="logo">

      <ul>
        <li
        v-for = "(icon, index) in icons"
        :key = "index"><a :href="icon.href" v-html="icon.iconName"></a></li>
        
      </ul>

    </div>
  </header>
</template>

<style lang="scss" scoped>

@use '../scss/partials/variabiles' as *;

.head{
  justify-content: space-between;
  align-items: center;
}

header {
  background-color: $PrimaryOrange;
  padding: 15px 0;
  position: fixed;
  width: 100%;
  box-shadow: 0px 5px 5px rgb(148, 148, 148);
  z-index: 999;
}

.container ul {
  li {
    list-style: none;
    display: inline-block;
    a {
      text-decoration: none;
      color: white;
    }
  }
  &:first-child li a {
    margin-right: 10px;
  }
  &:last-child li a {
    margin-left: 10px;
  }
}

.logo {
  width: 120px;
}
</style>
