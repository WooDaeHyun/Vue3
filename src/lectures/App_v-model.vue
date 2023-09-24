<template>
  <div>
    <h2>input Value</h2>
    <input type="text" v-model="inputValue" />
    <!-- :value="inputValue" @input="(event) => (inputValue = event.target.value)" -->
    <div>{{ inputValue }}</div>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const inputValue = ref('안녕!')

    return { inputValue }
  }
}
</script>

<style lang="scss" scoped></style>
