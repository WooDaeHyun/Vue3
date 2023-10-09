<template>
  <div>
    <postCreate @create-post="createPost" />
  </div>
</template>

<script>
import postCreate from './lectures/postCreate.vue'
export default {
  components: {
    postCreate
  },
  setup() {
    const createPost = (title) => {
      console.log(title)
    }
    return {
      createPost
    }
  }
}
</script>

<style lang="scss" scoped></style>
