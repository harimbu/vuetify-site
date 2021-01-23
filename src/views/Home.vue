<template>
  <div class="home">
    <Slide />
    <Gallery />
    <Post />
  </div>
</template>

<script>
import Slide from '@/components/Slide'
import Gallery from '@/components/Gallery'
import Post from '@/components/Post'
export default {
  components: { Slide, Gallery, Post }
}
</script>
