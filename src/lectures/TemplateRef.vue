<template>
  <div class="container py-4">
    <input type="text" ref="inputRef" />
  </div>
</template>

<script>
import { onMounted, ref } from 'vue'

export default {
  setup() {
    const inputRef = ref(null)

    onMounted(() => {
      inputRef.value.value = 'hello world'
      console.log(inputRef.value)
    })

    return { inputRef }
  }
}
</script>

<style lang="scss" scoped></style>
