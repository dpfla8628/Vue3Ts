<template>
  <ag-grid-vue
    style="width: 800px; height: 200px"
    class="ag-theme-alpine"
    :columnDefs="columnDefs"
    :rowData="rowData"
    :cellClicked="doubleClicked"
  >
  </ag-grid-vue>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import 'ag-grid-community/dist/styles/ag-grid.css'
import 'ag-grid-community/dist/styles/ag-theme-alpine.css'
import { AgGridVue } from 'ag-grid-vue3'

interface columnDefs {
  headerName: string
  field: string
}
interface rowData {
  make: string
  model: string
  price: number
}

export default defineComponent({
  name: 'App',
  components: {
    AgGridVue
  },
  setup () {
    return {
      columnDefs: [
        { headerName: 'Make', field: 'make' },
        { headerName: 'Model', field: 'model' },
        { headerName: 'Price', field: 'price' }
      ] as Array<columnDefs>,
      rowData: [
        { make: 'Toyota', model: 'Celica', price: 35000 },
        { make: 'Ford', model: 'Monde', price: 32000 },
        { make: 'Porsche', model: 'Boxier', price: 72000 }
      ] as Array<rowData>
    }
  },
  methods: {
    doubleClicked (): void {
      alert('test')
    }
  }
})
</script>
