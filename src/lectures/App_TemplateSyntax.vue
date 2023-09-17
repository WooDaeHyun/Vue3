<!-- 컴포지션 API -->
<template>
  <div>
    <h2>보간법</h2>
    <p>{{ message }}</p>
    <p v-once>{{ message }}</p>
    <button @click="handleClick">느낌표 추가</button>
    <hr />
    <h2>html</h2>
    <p v-html="rawHtml"></p>
    <hr />
    <div v-bind:title="dynamicTitle">안녕하세요</div>
    <hr />
    <div>{{ message.split('').reverse().join('') }}</div>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const message = ref('안녕하세요!!')
    const handleClick = () => {
      message.value += '!'
    }

    const rawHtml = ref('<strong>안녕하세요</strong>')

    const dynamicTitle = ref('마우스를 올려보아요!!!!')

    return {
      message,
      handleClick,
      rawHtml,
      dynamicTitle
    }
  }
}
</script>

<style lang="scss" scoped></style>
