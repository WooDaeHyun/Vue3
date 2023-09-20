<template>
  <div v-if="visible">Hello vue3!!</div>
  <button
    @click="
      () => {
        visible = !visible
      }
    "
  >
    click!
  </button>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const visible = ref(true)

    return { visible }
  }
}
</script>

<style lang="scss" scoped></style>
