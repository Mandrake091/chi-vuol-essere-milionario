<template>
  <main class="container">
    <div class="row justify-content-center mt-5">
      <div class="request text-center w-25">
        <h3 class="text-white">{{ domande[currentIndex].testo }}</h3>
      </div>
    </div>
    <div class="row mt-5">
      <div
        v-for="(domanda, index) in domande[currentIndex].risposte"
        :key="index"
        class="col-12 col-md-6"
      >
        <div class="answer">
          <a class="text-decoration-none" href="#"
            ><h4 @click="check(domanda)" class="text-white p-3">
              {{ domanda }}
            </h4></a
          >
        </div>
      </div>
    </div>
  </main>
</template>
<script>
export default {
  name: "GameComponent",
  data() {
    return {
      domande: [
        {
          id: 1,
          testo: "Qual è la capitale della Birmania?",
          risposte: ["Palermo", "Bologna", "Milano", "Livorno"],
          rispostaEsatta: "Milano",
        },
        {
          id: 2,
          testo: "Qual è la capitale della Francia?",
          risposte: ["Palermo", "Bologna", "Livorno", "Milano"],
          rispostaEsatta: "Palermo",
        },
        {
          id: 3,
          testo: "Qual è la capitale del Canada?",
          risposte: ["Palermo", "Livorno", "Bologna", "Milano"],
          rispostaEsatta: "Bologna",
        },
        {
          id: 4,
          testo: "Qual è la capitale della Turchia?",
          risposte: ["Livorno", "Bologna", "Roma", "Milano"],
          rispostaEsatta: "Milano",
        },
      ],
      currentIndex: 0,
    };
  },
  methods: {
    check(domanda) {
      let domandaScelta = domanda;
      let domandaGiusta = this.domande[this.currentIndex].rispostaEsatta;
      console.log(domanda);
      console.log(this.domande[this.currentIndex].rispostaEsatta);
      console.log(this.currentIndex);
      if (this.currentIndex == 3) {
        this.currentIndex = 0;
      }
      if (domandaScelta.localeCompare(domandaGiusta) == 0) {
        console.log("esatto!");

        this.currentIndex++;
      }
    },
  },
};
</script>
<style>
.request {
  border: 2px solid white;
}
.answer {
  border: 3px solid white;
  border-radius: 15px;
}
.row:nth-child(2) {
  row-gap: 50px;
}
.choose {
  background-color: red;
}
</style>
