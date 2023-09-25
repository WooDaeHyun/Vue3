<template>
  <div>{{ message }}</div>
  <input
    type="text"
    :value="message"
    @input="
      (event) => {
        message = event.target.value
      }
    "
  />
</template>

<script>
import { ref, watch } from 'vue'

export default {
  setup() {
    const message = ref('hello')

    watch(message, (newValue, oldValue) => {
      console.log('뉴', newValue)
      console.log('올드', oldValue)
    })
    return { message }
  }
}
</script>

<style lang="scss" scoped></style>
