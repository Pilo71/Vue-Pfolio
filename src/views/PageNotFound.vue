<template>
    <section>

        <RouterLink to="/">

            <img class="erreur hover2" src="../images/v4_5 - Copie.png" alt="logo" title="retour à la page d'acceuil !">
        </RouterLink>
        <h2 class="tipo2"> 404</h2>
        <p class="tipo3">error <br>page not found</p>

    </section>
    <router-view></router-view>
</template>
<script>
export default {
    name: "PageNotFound",
}
</script>