

<template>
  <section>
    <h1>Cécile Pilorger</h1>
    <img class="logo2" src="../images/v4_5 - Copie.png" alt="logo" />
    <h3 class="name">Des technologies à votre service</h3>
    <img class="portrait" src="../images/v13_22.png" alt="" />
    <p class="name position">Tout est dans le nom !<br>
      marvinEssentiel propose une gamme complète de solutions sur mesure
      pour la conception graphique et le développement de sites Web, adaptées à vos exigences et à votre budget.

    </p>
  </section>

  <section>

    <RouterLink to="/about" class="flex3">
      <h1 class=" left name hover">Projets</h1>
      <h2 class="contact2">Explorez quelques exemples ! </h2>
    </RouterLink>

  </section>
  <RouterView></RouterView>
  <section>
    <div class="flex1 ombre">
      <div class="marges"> <img class="galerie0 pointeur hover3" v-on:click="toggleModale" src="../images/002 c.v en ligne.jpg"
          alt="cv">
     <img class="galerie0 pointeur marge hover3" v-on:click="toggleModale2" src="../images/001 c.charges.jpg"
          alt="cahier des charges">
          <img class="galerie0 pointeur marge hover3" v-on:click="toggleModale3" src="../images/003 D.S.jpg" 
      alt="Dynamisme d'un site communautaire">
      </div>

    </div>

    <modale class="cadre2" v-bind:revele="revele" v-bind:toggleModale="toggleModale" v-bind:revele2="revele2"
      v-bind:toggleModale2="toggleModale2"></modale>
  </section>
  <section>


    <RouterLink to="/contact" class="flex3">
      <h1 class="name hover ">Contact</h1>
      <h2 class="contact1">Remplissez notre formulaire afin d'établir un premier contact !</h2>
    </RouterLink>
  </section>
  <RouterView></RouterView>
  <section>
    <div class="form">
      <form id="contact" action="">
        <div class="colonnes tipo">
          <label for="first-name">Nom et Prénom</label>
          <input class="style" type="text" v-model="form.firstName" name="firstName" id="form.firstName" />
        </div>
        <div class="colonnes tipo4">
          <label for="last-name">objet</label>
          <input class="style" type="text" v-model="form.objet" name="objet" id="form.objet" />
        </div>

        <div class="colonnes tipo5">
          <label for="message">Message</label>
          <textarea class="style2" type="text" v-model="form.message" name="message" id="form.message"></textarea>
        </div>
        <div class="send">

          <button class="bouton name2 center pointeur hover4" @click.prevent="sendData()">envoyer</button>
        </div>
        <div class=" send" v-for="form in errors">{{ form }}</div>

      </form>
    </div>
  </section>
</template>
<script>
import Modale from "./modales.vue"
import Modale2 from "./modales.vue"

export default {
  name: "home",
  data() {
    return {
      revele: false,
      revele2: false,
      errors: [],
      form: {
        firstName: null,
        objet: null,
        message: null,
      },
    }
  },
  components: {
    'modale': Modale,
    'modale2': Modale2,
  },
  methods: {
    toggleModale: function () {
      this.revele = !this.revele
    },
    toggleModale2: function () {
      this.revele2 = !this.revele2
    },
    sendData() {
      this.errors = [];

      if (!this.form.message) {
        this.errors.push("Tous les champs doivent étre remplis");
        return false;
      }
      this.form = {};

      alert("données envoyées");
    }
  }
}
</script>
