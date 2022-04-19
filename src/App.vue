<template>
  <div id="appWrapper" class="ph100">
    <div id="app" class="wrapper">
      <!-- GNB -->
      <gnb-component></gnb-component>

      <div class="container">
        <!-- Header-->
        <header-component></header-component>

        <!-- Content -->
        <content-component></content-component>
      </div>
    </div>

    <!-- Common Components -->
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import headerComponent from './components/header/header-component.vue'
import gnbComponent from './components/menu/gnb-component.vue'
import contentComponent from './components/content/content-component.vue'

import './assets/css/ui/style.css'

type DataType = {
  message: string
}

export default defineComponent({
  name: 'App',
  components: {
    'header-component': headerComponent,
    'gnb-component': gnbComponent,
    'content-component': contentComponent
  },
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
