<template>
  <button class="fancy-btn">
    <slot name="header"></slot>
    <slot name="body"></slot>
    <slot name="activeSlot">동적slot인데??</slot>
    <slot>Fallback Content!</slot>
  </button>
</template>

<script>
export default {
  setup() {
    return {}
  }
}
</script>

<style lang="scss" scoped>
.fancy-btn {
  color: #fff;
  background: linear-gradient(315deg, #42d392 25%, #647eff);
  border: none;
  padding: 5px 12px;
  margin: 5px;
  border-radius: 8px;
  cursor: pointer;
}
</style>
