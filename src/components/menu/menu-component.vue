<template>
  <li :id="data.name">
    <a href="javascript:"><span>{{data.name}}</span></a>
  </li>
</template>

<script lang="ts">

import { defineComponent } from 'vue'

export default defineComponent({
  name: 'menu-component',
  props: {
    data: {
      type: Object,
      required: true
    }
  }
})
</script>
