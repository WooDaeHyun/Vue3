<template>
  <div>
    <span class="badge bg-secondary">{{ type === 'news' ? '뉴스' : '공지사항' }}</span>
    <div>{{ title }}</div>
    <p>{{ contents }}</p>
  </div>
</template>

<script lang="ts">
export default {
  props: {
    title: {
      type: String,
      default: 'news'
    },
    contents: {
      type: String,
      default: '내용!'
    },
    type: {
      type: String,
      required: true
    }
  },
  setup(props) {
    console.log(props.contents)
    console.log(props.title)
    console.log(props.type)

    return {}
  }
}
</script>

<style lang="scss" scoped></style>
