<template>
  <q-page padding>
    <q-input v-model="searchQuery" label="Traži knjigu" />

    <div class="q-gutter-sm q-mb-md">
      <q-checkbox v-model="searchByTitle" label="Po naslovu" />
      <q-checkbox v-model="searchByAuthor" label="Po autoru" />
    </div>

    <q-btn label="Traži" color="primary" @click="searchBooks" />

    <q-table
      :rows="filtered"
      :columns="columns"
      row-key="id"
      class="q-mt-md"
    >
      <template v-slot:body-cell-slika="props">
        <q-td :props="props">
          <img :src="props.row.slika" width="50" />
        </q-td>
      </template>
    </q-table>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const searchQuery = ref('')
const searchByTitle = ref(true)
const searchByAuthor = ref(false)

const books = [
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

const filtered = ref([])

function searchBooks() {
  const q = searchQuery.value.toLowerCase()
  filtered.value = books.filter(book => {
    return (
      (searchByTitle.value && book.naslov.toLowerCase().includes(q)) ||
      (searchByAuthor.value && book.autor.toLowerCase().includes(q))
    )
  })
}

const columns = [
  {
    name: 'id',
    label: 'ID',
    field: 'id',
    align: 'left',
    sortable: true,
    style: { fontSize: '14px' },
    headerStyle: { fontSize: '18px' }
  },
  {
    name: 'naslov',
    label: 'Naslov',
    field: 'naslov',
    align: 'left',
    sortable: true,
    style: { fontSize: '14px' },
    headerStyle: { fontSize: '18px' }
  },
  {
    name: 'autor',
    label: 'Autor',
    field: 'autor',
    align: 'left',
    sortable: true,
    style: { fontSize: '14px' },
    headerStyle: { fontSize: '18px' }
  },
  {
    name: 'opis',
    label: 'Opis',
    field: 'opis',
    align: 'left',
    sortable: false,
    style: { fontSize: '14px' },
    headerStyle: { fontSize: '18px' }
  },
  {
    name: 'slika',
    label: 'Slika',
    field: 'slika',
    align: 'center',
    sortable: false,
    style: { fontSize: '14px' },
    headerStyle: { fontSize: '18px' }
  },
  {
    name: 'status',
    label: 'Status',
    field: 'status',
    align: 'center',
    sortable: true,
    style: { fontSize: '14px' },
    headerStyle: { fontSize: '18px' }
  }
]
</script>
