<template>
  <App_props title="제목" contents="내용" type="타입"></App_props>
  <App_props :title="post.title" :contents="post.contents" :type="post.type"></App_props>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import App_props from './lectures/App_props.vue'

const post = ref({
  title: '제목제목제목제목제목',
  contents: '내용내용내용내용내용내용',
  type: 'news'
})
</script>

<style lang="scss" scoped></style>
