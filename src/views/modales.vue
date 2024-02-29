<template>
    <div class=" modale " v-if="revele">
        <div class="overlay pointeur" v-on:click="toggleModale"></div>
        <div class="cadre2">
            <div class="boutonModale pointeur" v-on:click="toggleModale">
                <h4>X</h4>
            </div>
            <h2>C.V en ligne</h2>
            <div>
                <p>Date de création : 15/06/2023</p>
            </div>
            <div>
                <p>Technologies utilisées : HTML,CSS</p>
            </div>
            <div>
                <p>Liens : <a class="style" href="https://github.com/Pilo71/Mon-CV.git" target="_blank">
                        Github<img class="taille" src="../images/github.png" alt=""></a>
                </p>

            </div>
        </div>
    </div>
    <div class=" modale " v-if="revele2">
        <div class="overlay pointeur" v-on:click="toggleModale2"></div>
        <div class="cadre2">
            <div class="boutonModale pointeur" v-on:click="toggleModale2">
                <h4>X</h4>
            </div>
            <h2>Cahier des charges</h2>
            <div>
                <p>Date de création : 23/07/2023</p>
            </div>
            <div>
                <p>Technologies utilisées : Photoshop</p>
            </div>
            <div>

                <p>Liens : <a class="style" href="/src/assets/Classeur Cahier des charges.pdf" target="_blank">
                        PDF<img class="taille " src="../images/pdf.png" alt=""></a>
                </p>


            </div>

        </div>
    </div>
    <div class=" modale " v-if="revele3">
        <div class="overlay pointeur" v-on:click="toggleModale3"></div>
        <div class="cadre2">
            <div class="boutonModale pointeur" v-on:click="toggleModale3">
                <h4>X</h4>
            </div>
            <h2 class="marge3">Dynamisme d'un site </h2>
            <h2>communautaire</h2>
            <div>
                <p>Date de création : 20/08/2023</p>
            </div>
            <div>
                <p>Technologies utilisées : HTML,CSS,J.S.</p>
            </div>
            <div>
                <p>Liens : <a class="style" href="https://github.com/Pilo71/devoirdynamiercommentairesjs.git"
                        target="_blank">
                        Github<img class="taille" src="../images/github.png" alt=""></a>
                </p>

            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: "modale",


    props: ['revele', 'toggleModale', 'revele2', 'toggleModale2', 'revele3', 'toggleModale3'],



}

</script>
<style scoped>
.overlay {
    background: rgba(0, 0, 0, 0.6);

    position: fixed;
    width: 100%;
    height: 100%;
    right: 0;
    left: 0;
    top: 0;
    bottom: 0;
}



.boutonModale {
    background: red;
    width: 20px;
    height: 20px;
    margin-left: 215px;
    margin-top: 4px;
    display: flex;
    justify-content: center;
    align-items: center;
}

h4 {
    color: aliceblue;
}

.pointeur {
    cursor: grab;
}

.flex {
    display: flex;
}

.style {
    color: black;
    font-family: ABeeZee;
    text-decoration: none;
    filter: drop-shadow(10px 5px 7px rgba(0, 0, 0, 0.25));
}

.taille {
    width: 15px;
    margin-bottom: -3px;

}
</style>    