<template>
  <q-page padding>
    <q-form @submit.prevent="potvrdiRegistraciju">

      <q-input v-model="ime" label="Ime" filled />
      <q-input v-model="prezime" label="Prezime" filled />
      <q-input v-model="email" label="Email" type="email" filled />
      <q-input v-model="korisnickoIme" label="Korisničko ime" filled />
      <q-input v-model="lozinka" label="Lozinka" type="password" filled />

      <q-btn label="Potvrdi" type="submit" color="primary" />
    </q-form>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const ime = ref('')
const prezime = ref('')
const email = ref('')
const korisnickoIme = ref('')
const lozinka = ref('')

function potvrdiRegistraciju() {
  const noviKorisnik = {
    ime: ime.value,
    prezime: prezime.value,
    email: email.value,
    korisnickoIme: korisnickoIme.value,
    lozinka: lozinka.value
  }

  console.log('Registracija:', noviKorisnik)
}
</script>
