<template>
  <v-container>
    <v-toolbar flat>
      <v-toolbar-title class="logo"><router-link to="/">photography</router-link></v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-btn text color="grey darken-3" v-for="item in items" :key="item.id" :to="item.to">{{ item.title }}</v-btn>
      </v-toolbar-items>
    </v-toolbar>
  </v-container>
</template>
<script>
export default {
  data() {
    return {
      items: [
        { id: 1, title: 'home', to: '/' },
        { id: 2, title: 'about', to: '/about' },
        { id: 3, title: 'contact', to: '/contact' }
      ]
    }
  }
}
</script>
