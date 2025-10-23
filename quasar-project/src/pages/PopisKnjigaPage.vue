<template>
  <q-page padding>
    <!-- content -->
         <q-toolbar class="bg-grey-9 text-white">
      <q-btn flat round dense>
        <q-icon name="menu" />
      </q-btn>
      <q-toolbar-title>
        Toolbar
      </q-toolbar-title>
      <q-btn flat round dense>
        <q-icon name="more_vert" />
      </q-btn>
    </q-toolbar>
    
      <q-item clickable v-ripple>
        <q-item-section thumbnail>
          <img src="https://www.svijet-knjige.com/spijunska.obala.ai.13138.260.380.1..jpg">
        </q-item-section>
        <q-item-section>Špijunska obala</q-item-section>
      </q-item>

      <q-item clickable v-ripple>
        <q-item-section thumbnail>
          <img src="https://www.svijet-knjige.com/neukrotivi.grof.ai.13470.260.380.1.c-n.jpg">
        </q-item-section>
        <q-item-section>Neukrotivi grof</q-item-section>
      </q-item>

      <q-item clickable v-ripple>
        <q-item-section thumbnail>
          <img src="https://www.svijet-knjige.com/bog.sume.ai.13469.260.380.1.km.jpg">
        </q-item-section>
        <q-item-section>Bog šume</q-item-section>
      </q-item>
  </q-page>
</template>

<script setup>
//
</script>
