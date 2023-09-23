<template>
  <div>
    <span v-text="msg"></span>
    <span>{{ msg }}</span>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const msg = ref('안녕하세요')

    return { msg }
  }
}
</script>

<style lang="scss" scoped></style>
