<template lang="pug">
  section.hero.is-success
    .hero.head
      header.nav
        .container
          .nav-left
            .nav-item
              strong Platzi Music App
          .nav-right.nav-menu
            router-link.nav-item(to="/") Buscar
            router-link.nav-item(to="/about") Nosotros

    .hero-body
      .container.has-text-centered
        h1.title Plazi Music
        h2.subtitle Canciones desde api
        pm-player
</template>

<script>
import PmPlayer from '@/components/Player.vue'

export default {
  components: { PmPlayer }

}
</script>
