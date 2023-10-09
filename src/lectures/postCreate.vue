<template>
  <div>
    <!-- <button class="btn btn-primary" @click="$emit('createPost')">button</button> -->
    <input type="text" class="form-control" v-model="title" />
    <button class="btn btn-primary" @click="createPost">저장!!!</button>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  // emits: ['createPost'],
  emits: {
    createPost: (newTitle) => {
      if (!newTitle) {
        return false
      }
      return true
    }
  },
  setup(props, context) {
    context.emit
    const title = ref('')
    const createPost = () => {
      context.emit('createPost', title.value)
    }
    return { createPost, title }
  }
}
</script>

<style lang="scss" scoped></style>
