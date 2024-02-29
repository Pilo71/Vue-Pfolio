<template>
  <section>
    <div class="decal2">
      <h1 class="name3 ">Projets</h1>
      <h2 class="contact1">Explorez quelques exemples ! </h2>
    </div>
  </section>
  <section>
    <div>
       <img class="galerie1 pointeur hover3" v-on:click="toggleModale" src="../images/002 c.v en ligne.jpg" alt="cv"></div>
       <img class="galerie1 pointeur marge hover3" v-on:click="toggleModale2" src="../images/001 c.charges.jpg"
      alt="cahier des charges">
      <img class="galerie1 pointeur marge hover3" v-on:click="toggleModale3" src="../images/003 D.S.jpg"
      alt="Dynamisme d'un site communautaire">
       
    <modale v-bind:revele="revele" v-bind:toggleModale="toggleModale" v-bind:revele2="revele2"
      v-bind:toggleModale2="toggleModale2"></modale>
  </section>
</template> 
<script>
import Modale from "./modales.vue"
import Modale2 from "./modales.vue"
export default {
  name: "About",

  data() {
    return {
      revele: false,
      revele2: false
    }
  },
  components: {
    'modale': Modale,
    'modale2': Modale2
  },
  methods: {
    toggleModale: function () {
      this.revele = !this.revele
    },
    toggleModale2: function () {
      this.revele2 = !this.revele2
    }
  }

}

</script>
<style scoped>
.pointeur {
  cursor: grab;
}

.bouton {
  background: #c4ebd3;
  color: black;
  margin-top: 180px;
  width: 130px;
  height: 30px;

}

.marge {
  margin-top: 70px;
}
</style> 
   


