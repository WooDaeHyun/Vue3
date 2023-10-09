<template>
  <div class="container py-4" ref="testDiv">
    <input type="text" ref="testInput" value="hello world" />
    <input type="text" v-model="message" />
  </div>
</template>

<script>
import { onBeforeMount, onBeforeUpdate, onMounted, onUpdated, ref } from 'vue'

export default {
  setup() {
    const message = ref('아뇨오오옹~')
    const testInput = ref(null)

    onBeforeUpdate(() => {
      console.log('업데이트 직전!')
    })

    onUpdated(() => {
      console.log('업데이트 직후!')
    })

    onMounted(() => {
      console.log('마운트 후!')
      console.log(testInput.value)
      console.log(testInput.value.value)
    })

    onBeforeMount(() => {
      console.log('마운트 전!')
    })
    console.log('setup')
    //setup 단계는 creation 단계이므로 접근 불가!
    console.log(testInput.value)

    return { testInput, message }
  }
  // created() {
  //   console.log('created')
  // },
  // beforeCreate() {
  //   console.log('beforeCreated')
  // }
}
</script>

<style lang="scss" scoped></style>
