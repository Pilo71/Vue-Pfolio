<template>
  <section>
    <div class="decal2">
      <h1 class="name3 ">Contact</h1>
      <h2 class="contact1">Remplissez notre formulaire afin d'établir un premier contact !</h2>
    </div>
    <div class="form">
      <form id="contact" action="">

        <div class="colonnes tipo">
          <label for="first-name">Nom et Prénom</label>
          <input class="style" type="text" v-model="form.firstName" name="firstName" id="form.firstName" />
        </div>
        <div class="colonnes tipo4">
          <label for="last-name">objet</label>
          
          <input class="style" type="text" v-model="form.objet" name="objet" id="form.objet"  />
        </div>

        <div class="colonnes tipo5">
          <label for="message">Message</label>
          <textarea class="style2" type="text" v-model="form.message" name="message" id="form.message"></textarea>
        </div>
        <div class="send">
          <button class="bouton name2 center hover4" @click.prevent="sendData()">envoyer</button>
        </div>
        <div class=" send" v-for="form in errors">{{ form }}</div>
      </form>
    </div>
  </section>
</template>
<script>
export default {
  name: "contact",
  data() {
    return {
      errors: [],
      form: {
        firstName: null,
        objet: null,
        message: null,
      },
    };
  },
  methods: {
    sendData() {
      this.errors = [];
      if (!this.form.message) {
        this.errors.push("Tous les champs doivent étre remplis");
        return false;
      }
      this.form = {};
      alert("données envoyées");
    }
  },

};
</script>