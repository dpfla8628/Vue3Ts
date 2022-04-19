<template>
  <header class="vue">
    <h1 class="logo"><a :class="vue" ref="logotag">{{projectName}}</a></h1>
    <nav class="gnb">
      <ul class="gnb-menu">
        <menu-component v-for="(menu, index) in topMenus " :key="index" :data="menu"></menu-component>
      </ul>
    </nav>
  </header>
</template>
<script lang="ts">
import { defineComponent } from 'vue'
import menu from './menu-component.vue'

interface menus {
  name: string
  // field: string
}

export default defineComponent({
  name: 'gnb-component',
  components: {
    'menu-component': menu
  },
  data () {
    return {
      topMenus: [
        { name: 'menu1' },
        { name: 'menu2' }
      ] as Array<menus>
    }
  },
  methods: {
  }
})
</script>
