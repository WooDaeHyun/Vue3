<template>
  <div>{{ text }}</div>
</template>

<script>
import { inject } from 'vue'

export default {
  setup() {
    const text = inject('message')
    return { text }
  }
}
</script>

<style lang="scss" scoped></style>
