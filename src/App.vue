<template>
  <v-app>
    <v-app-bar color="white" app flat>
      <Header />
    </v-app-bar>
    <v-main>
      <router-view></router-view>
    </v-main>
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
