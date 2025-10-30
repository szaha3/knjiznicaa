<template>
  <q-page padding>
    <!-- Toolbar -->
    <q-toolbar class="bg-grey-9 text-white">
      <q-btn flat round dense>
        <q-icon name="menu" />
      </q-btn>
      <q-toolbar-title>
        Popis Knjiga
      </q-toolbar-title>
      <q-btn flat round dense>
        <q-icon name="more_vert" />
      </q-btn>
    </q-toolbar>

    <q-table
      title="Tablica knjiga"
      :rows="rows"
      :columns="columns"
      row-key="id"
      virtual-scroll
      :rows-per-page-options="[5, 10, 20]"
      class="q-mt-lg"
    >
      <template v-slot:body-cell-slika="props">
        <q-td :props="props" class="text-center">
          <img
            :src="props.row.slika"
            alt="Slika knjige"
            style="width: 60px; height: auto; border-radius: 4px;"
          />
        </q-td>
      </template>
    </q-table>
  </q-page>
</template>

<script setup>
const columns = [
  { name: 'id', label: 'ID', field: 'id', align: 'left', sortable: true },
  { name: 'naslov', label: 'Naslov', field: 'naslov', align: 'left', sortable: true },
  { name: 'autor', label: 'Autor', field: 'autor', align: 'left', sortable: true },
  { name: 'opis', label: 'Opis', field: 'opis', align: 'left' },
  { name: 'slika', label: 'Slika', field: 'slika', align: 'center' },
  { name: 'status', label: 'Status', field: 'status', align: 'center', sortable: true }
]

const rows = [
  {
    id: 1,
    naslov: 'Mali Princ',
    autor: 'Antoine de Saint-Exupéry',
    opis: 'Filozofska bajka o prijateljstvu i ljubavi.',
    slika: 'https://www.svijet-knjige.com/mali.princ.ai.6873.260.380.1..jpg',
    status: 'slobodna'
  },
  {
    id: 2,
    naslov: 'Zločin i kazna',
    autor: 'Fjodor Dostojevski',
    opis: 'Psihološki roman o moralnim dilemama i iskupljenju.',
    slika: 'https://ezop-antikvarijat.hr/wp-content/uploads/2019/11/307208392_1073629653525853_5495292819280031631_n.jpg',
    status: 'zauzeta'
  },
  {
    id: 3,
    naslov: 'Bog šume',
    autor: 'Liz Moore',
    opis: 'Fantastična priča o vilinskom svijetu i ljudima.',
    slika: 'https://www.svijet-knjige.com/bog.sume.ai.13469.260.380.1.km.jpg',
    status: 'slobodna'
  }
]
</script>
