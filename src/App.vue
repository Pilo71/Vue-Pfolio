<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <header>
    
    <RouterLink to="/">
    
  <img class="logo logoHover" src="../src/images/marvinEssentiel.png" alt="logo" />
    </RouterLink>
    <nav>
    
      <ul class="nav">
        <RouterLink to="/" class="decoration">

          <li class="  name2 bouton hover4 ">Acceuil</li>
        </RouterLink>
        <RouterLink to="/about" class="decoration">
          <li class="bouton name2  hover4">Projets</li>
        </RouterLink>
        <RouterLink to="/contact" class="decoration">
          <li class="bouton name2  hover4">Contact</li>
        </RouterLink>
      </ul>     
    </nav>
      
    

  </header>

  <RouterView />
</template>

<style scoped>
nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: -66px;
  margin-bottom: 1px;
}

.hover4:hover {
  color: #c4ebd3;
  font-family: "ABeeZee";
  font-size: 16px;
}

.decoration {
  text-decoration: none;
}
</style>
