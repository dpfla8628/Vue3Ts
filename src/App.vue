<template>
  <h1>Hello</h1>
  <div>{{ message }}</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

type DataType = {
  message: string
}

export default defineComponent({
  data (): DataType {
    return {
      message: ''
    }
  },
  created () {
    this.initMessage()
  },
  methods: {
    initMessage (): void {
      this.message = 'World'
    }
  }
})
</script>
