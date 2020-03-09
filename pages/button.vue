<template lang="pug">
.container.mt-5.text-center.flex.flex-col
  div.mx-auto.p-3
    p.bold {{capacity}}
  button.btn.btn-info.block.mx-auto.my-2(class='w-2/12' @click='increment') incrementer
  button.btn.btn-info.block.mx-auto(class='w-2/12' @click='double') doubler
</template>

<script>
import { ref } from '@vue/composition-api'
export default {
  /*
  data() {
    return {}
  }

  */
  setup(props) {
    const capacity = ref(0)
    const increment = () => {
      capacity.value++
    }
    const double = () => {
      capacity.value *= 2
    }
    return { capacity, increment, double }
  }
}
</script>

<style lang="stylus" scoped>
.btn
  @apply rounded px-3 py-2 text-white font-bold uppercase
.btn-info
  @apply bg-blue-400
</style>
