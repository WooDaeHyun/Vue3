<template>
  <div class="p-3 bg-danger">
    <button class="btn btn-primary" type="button" v-bind="$attrs">버튼 Click!!!!</button>
  </div>
</template>

<script>
export default {
  // non-props 속성은 부모요소에서 자식요소의 최상단 요소로 전달된다.
  // 아래 설정을 통해 상속을 막을 수 있음!
  inheritAttrs: false,
  setup() {
    return {}
  }
}
</script>

<style lang="scss" scoped></style>
