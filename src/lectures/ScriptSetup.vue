<template>
  <div>{{ props.type }}</div>
  <div>{{ props.foo }}</div>
  <div>{{ props.hello }}</div>
</template>

<script setup>
const props = defineProps({
  type: String,
  foo: Number,
  hello: String
})
</script>

<style lang="scss" scoped></style>
