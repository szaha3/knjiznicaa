<template>
  <q-page padding>
    <!-- content -->
    
     <h1>{{ poruka}}</h1>
     <p v-html="tijelo"></p>
     <p v-html="htmlTekst"></p>
     <p v-text="htmlTekst"></p>
     <p v-for="item in days" :key="item">
      <button>
        {{ item }}
      </button>
     </p>

     <p v-for="item in days" :key="item">
      <button v-if="item=='pon'">
        {{ item }} *
      </button>

      <button v-else v-show="false">
        {{ item }}
      </button>
     </p>
      
     <a :href="link.url" :target="link.target"> {{link.text}} </a>

     <q-input color="purple-12" v-model="text" label="Ime" @keyup="log()"> </q-input>
     <q-input color="purple-12" v-model="text" label="Prezime" @keyup="log()"> </q-input>


     
     
  </q-page>

</template>

<script setup>
//
  const poruka="test page"
  const tijelo="tekst na starnici"
  const htmlTekst="<p><b>Formatirani teskt</b> na stranici</p>"
  const days=['pon','uto','sri']

  const link = {
    url: 'http://www.google.com',
    target: '_blank',
    text: 'Google'
  }

  import { ref } from 'vue'
  const text = ref('')
  text.value = "Ime"

  function log() {
    console.log(text.value)
  }
  




</script>
