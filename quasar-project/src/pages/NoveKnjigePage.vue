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
      <img src="https://www.svijet-knjige.com/mali.princ.ai.6873.260.380.1..jpg">

      <q-card-section>
        <div class="text-h6">MALI PRINC</div>
        <div class="text-subtitle2">ANTOINE DE SAINT-EXUPERY </div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ knjiga1 }}
      </q-card-section>
    </q-card>

    <q-card class="my-card">
      <img src="https://ezop-antikvarijat.hr/wp-content/uploads/2019/11/307208392_1073629653525853_5495292819280031631_n.jpg">

      <q-card-section>
        <div class="text-h6">ZLOČIN I KAZNA</div>
        <div class="text-subtitle2">FJODOR MIHAJLOVIČ DOSTOJEVSKI</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ knjiga2 }}
      </q-card-section>
    </q-card>

    <q-card class="my-card">
      <img src="https://www.svijet-knjige.com/bog.sume.ai.13469.260.380.1.km.jpg">

      <q-card-section>
        <div class="text-h6">BOG ŠUME</div>
        <div class="text-subtitle2">LIZ MOORE</div>
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
      knjiga1: 'Ovo neveliko, ali iznimno duboko i nadahnjujuće djelo očaralo je čitatelje svih uzrasta diljem svijeta, o čemu svjedoči i to da je knjiga prevedena na preko 200 svjetskih jezika, te prodana u više od 80 milijuna primjeraka, što je čini jednom od najprodavanijih knjiga na svijetu. Jedna od njezinih posebnosti je i u tome što ju je ilustrirao sam autor, kako bi što vjernije dočarao svoje likove.',
      knjiga2: 'Zločin i kazna, jedno od najpoznatijih djela Fjodora Mihajloviča Dostojevskog, nije samo roman, već putovanje u najskrivenije zakutke ljudske duše. Ovo remek-djelo iz 1866. godine, koje je autora proslavilo kao majstora psihološkog romana, i danas na čitatelja ostavlja snažan dojam zbog svoje bezvremenske tematike. Njegov utjecaj seže daleko izvan književnih krugova, u filozofiju, psihologiju i popularnu kulturu te potpuno opravdano možemo reći da je ovo djelo pomoglo oblikovati suvremeno razumijevanje morala, pravde i duhovnosti.',
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
