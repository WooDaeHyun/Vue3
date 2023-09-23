<template>
  <div>
    <span v-text="msg"></span>
    <hr />
    <span>{{ msg }}</span>
    <hr />
    <span v-html="strong"></span>
    <hr />
    <span v-text="strong"></span>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const msg = ref('안녕하세요')
    const strong = ref('<strong>강조!</strong>')

    return { msg, strong }
  }
}
</script>

<style lang="scss" scoped></style>
