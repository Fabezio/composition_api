<template lang="pug">
#list
  h1 Liste
  p Membres de la famille
    |
    |
    span.text-italic ({{members.length}})
    |:
  ul
    div(v-for='(member, i) in members' :key='i')
      li() {{member}}

</template>

<script>
import { ref } from '@vue/composition-api'
export default {
  setup(props) {
    const members = ref(['Papa', 'Maman', 'Cassy'])
    return { members }
  }
}
</script>

<style lang="stylus" scoped>
#list
  margin 5em auto
  width 25%
h1
  font-weight bold
  font-size 2em
  text-align left
li
  list-style '> ' inside
  text-indent 0.5em
</style>
