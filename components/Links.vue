<template lang="pug">
.flex.justify-center
  NuxtLink(to='/') Accueil
  span.mx-2 |
  NuxtLink(to='/button') Bouton
</template>
<script>
export default {}
</script>

<style lang="stylus" scoped>
.nuxt-link-exact-active
  color yellowgreen
  font-weight bold
</style>
