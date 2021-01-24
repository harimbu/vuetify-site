<template>
  <v-main>
    <div class="slide">
      <v-carousel hide-delimiters cycle>
        <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src">
          <v-row class="fill-height" align="center" justify="center">
            <div class="title">{{ item.title }}</div>
          </v-row>
        </v-carousel-item>
      </v-carousel>
    </div>
  </v-main>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          src: require('../assets/images/img-carousel1.jpg'),
          title: 'We are creative'
        },
        {
          src: require('../assets/images/img-carousel2.jpg'),
          title: 'We are hard worker'
        },
        {
          src: require('../assets/images/img-carousel3.jpg'),
          title: 'We are professional'
        }
      ]
    }
  }
}
</script>
