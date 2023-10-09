<template>
  <provide_inject></provide_inject>
</template>

<script>
import { provide } from 'vue'
import provide_inject from './lectures/provide_inject.vue'

export default {
  components: {
    provide_inject
  },
  setup() {
    provide('message', '아따 복잡허다')

    return {}
  }
}
</script>

<style lang="scss" scoped></style>
