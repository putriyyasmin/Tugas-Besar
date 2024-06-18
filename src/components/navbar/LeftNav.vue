<template>
    <v-navigation-drawer v-model="drawer" :rail="rail" permanent @click="rail = false">
      <v-list-item prepend-avatar="https://cdn-ssl-devio-img.classmethod.jp/wp-content/uploads/2019/03/eyecatch-vue.png" title="Aplikasi Pendaftraan" nav>
        <template v-slot:append>
          <v-btn icon="mdi-chevron-left" variant="text" @click.stop="rail =!rail"></v-btn>
        </template>
      </v-list-item>
  
      <v-divider></v-divider>
  
      <v-list density="compact" nav>
        <v-list-item
          v-for="(item, index) in navItems"
          :key="index"
          :prepend-icon="`mdi-${item.icon}`"
          :title="item.title"
          :value="item.value"
          :to="item.to"
        ></v-list-item>
      </v-list>
    </v-navigation-drawer>
  </template>
  
  <script>
  export default {
    data() {
      return {
        drawer: true,
        rail: true,
        navItems: [
          { icon: 'home', title: 'Home', value: 'home', to: '/' },
          { icon: 'account', title: 'Pendaftaran', value: 'lomba', to: '/form' },
        ]
      }
    }
  }
  </script>