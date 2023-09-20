<template>
  <div>
    <div v-bind:style="styleObject">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab odit soluta tempore minus itaque
      nesciunt, sequi dolor et, vel placeat reiciendis perferendis possimus, dignissimos fuga alias
      temporibus. Ipsam, aliquid aut!
    </div>
    <button @click="fontSize++">+</button>
    <button @click="fontSize--">-</button>
  </div>
</template>

<script>
import { computed, reactive, ref } from 'vue'

export default {
  setup() {
    // const styleObject = reactive({
    //   color: 'red',
    //   fontSize: '20px'
    // })

    const fontSize = ref(13)

    const styleObject = computed(() => {
      return {
        color: 'blue',
        fontSize: fontSize.value + 'px'
      }
    })

    return { styleObject, fontSize }
  }
}
</script>

<style lang="scss" scoped></style>
