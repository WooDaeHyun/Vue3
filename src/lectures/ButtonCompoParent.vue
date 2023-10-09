<template>
  <div>
    <ButtonCompo v-on:click="sayHello"></ButtonCompo>
    <!-- $attrs 객체를 활용하여 non-props 상속을 거부하였지만 특정 요소에 non-props 들을 전달할 수 있음 -->
  </div>
</template>

<script setup>
import ButtonCompo from '../src/lectures/ButtonCompo.vue'

const sayHello = () => {
  alert('안녕하세요!')
}
</script>

<style lang="scss" scoped></style>
