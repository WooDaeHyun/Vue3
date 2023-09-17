<template>
  <div @click="addMessage">{{ message }}</div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const message = ref('하이호이')
    const addMessage = () => {
      message.value += '!'
    }
    return {
      message,
      addMessage
    }
  }
}
</script>

<style lang="scss" scoped></style>
