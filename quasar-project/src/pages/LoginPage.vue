<template>
  <q-page padding>
    <q-form @submit.prevent="potvrdiPrijavu" class="q-gutter-md">

      <q-input v-model="korisnickoIme" label="Korisničko ime" filled />
      <q-input v-model="lozinka" label="Lozinka" type="password" filled />

      <q-btn label="Potvrdi" type="submit" color="primary" />
    </q-form>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const korisnickoIme = ref('')
const lozinka = ref('')

function potvrdiPrijavu() {
  const podaciZaPrijavu = {
    korisnickoIme: korisnickoIme.value,
    lozinka: lozinka.value
  }

  console.log('Login:', podaciZaPrijavu)
}
</script>
