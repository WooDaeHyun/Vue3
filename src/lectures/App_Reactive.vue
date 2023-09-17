<template>
  <div>
    <p>이름</p>
    <button @click="add">{{ reactiveObj.name }}</button>
    <p>나이</p>
    <div>{{ reactiveObj.age }}</div>
  </div>
</template>

<script>
import { reactive } from 'vue'

export default {
  setup(props, context) {
    console.log(props, context)

    const reactiveObj = reactive({
      name: '우대현',
      age: 31
    })
    const add = () => {
      reactiveObj.age += reactiveObj.age
    }

    return {
      reactiveObj,
      add
    }
  }
}
</script>

<style lang="scss" scoped></style>
