<template>
  <q-page padding>
    <!-- content -->
         <q-toolbar class="bg-grey-9 text-white">
      <q-btn flat round dense>
        <q-icon name="menu" />
      </q-btn>
      <q-toolbar-title>
        Nove knjige
      </q-toolbar-title>
      <q-btn flat round dense>
        <q-icon name="more_vert" />
      </q-btn>
    </q-toolbar>
  
    <div class="q-pa-md row items-start q-gutter-md"> 
    <q-card class="my-card">
      <img src="https://www.svijet-knjige.com/spijunska.obala.ai.13138.260.380.1..jpg">

      <q-card-section>
        <div class="text-h6">Špijunska obala</div>
        <div class="text-subtitle2">by Tess Gerritsen</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ knjiga1 }}
      </q-card-section>
    </q-card>

    <q-card class="my-card">
      <img src="https://www.svijet-knjige.com/neukrotivi.grof.ai.13470.260.380.1.c-n.jpg">

      <q-card-section>
        <div class="text-h6">Neukrotivi grof</div>
        <div class="text-subtitle2">by JULIE ANNE LONG</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ knjiga2 }}
      </q-card-section>
    </q-card>

    <q-card class="my-card">
      <img src="https://www.svijet-knjige.com/bog.sume.ai.13469.260.380.1.km.jpg">

      <q-card-section>
        <div class="text-h6">Bog šume</div>
        <div class="text-subtitle2">by LIZ MOORE</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ knjiga3 }}
      </q-card-section>
    </q-card>

    </div>

  </q-page>
</template>

<script>
export default {
  setup () {
    return {
      knjiga1: 'Maggie Bird ostavila je špijunski život iza sebe nakon što je jedna od njezinih misija završila tragedijom. Danas živi povučenim životom, na farmi u tihom gradiću na obalama snježnog Mainea. No, kada se u njezinu prilazu pojavi tijelo, shvaća da je njena prošlost ipak nije zaboravila i da netko želi njezinu smrt.',
      knjiga2: 'Kapetan Flint, kopile miješane rase, gusar, trgovac i novoimenovani grof od Ardmaya, ne pokorava se nikome osim sebi. Violet Redmond, ljepotica britkog jezika i nemirna duha, odbija sve prosce. Kada posumnja da se iza krinke zloglasnog pirata Le Chata skriva njen nestali brat Lyon, Violet se potajno ukrca na Flintov brod kako bi ga spasila. Flint, zadivljen njezinom hrabrošću i čarima, ubrzo shvaća da su oboje uhvaćeni u vrtlogu strasti gdje granica između požude i opasnosti postaje nemilosrdno tanka',
      knjiga3: 'Rano jutro u kolovozu 1975. unosi nepopravljiv razdor u prestižnu obitelj Van Laar. Krevet njihove trinaestogodišnje kćeri Barbare u elitnom ljetnom kampu je prazan, nitko ne zna kamo je otišla, a šuma koja okružuje kamp ne oprašta nijedan pogrešan korak.'
    }
  }
}
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 250px
</style>
