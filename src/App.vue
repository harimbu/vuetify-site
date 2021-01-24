<template>
  <v-app>
    <v-app-bar color="white" app flat absolute>
      <Header />
    </v-app-bar>
    <router-view></router-view>
    <v-footer padless color="white">
      <Footer />
    </v-footer>
  </v-app>
</template>

<script>
import Header from '@/components/Header'
import Footer from '@/components/Footer'
export default {
  components: { Header, Footer }
}
</script>
