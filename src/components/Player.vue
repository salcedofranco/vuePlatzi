<template lang="pug">
  .content
    p
      img(
        v-if="track && track.album",
        :src="track.album.images[0].url")
    p
      strong {{ track.name }}
      small [{{track.duration_ms}}]
    p
      audio(controls, :src="track.preview_url")
</template>

<script>
export default {

  data () {
    return {
      track: {}
    }
  },

  created () {
    this.$bus.$on('set-track', (track) => {
      this.track = track
    })
  }
}
</script>

<style scoped>
  img {
    width: 124px;
    border-radius: 50% ;

  }

</style>
