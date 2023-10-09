<template>
  <FancyButton>Click!<span style="color: red">@@@</span></FancyButton>
  <FancyButton></FancyButton>
  <FancyButton>
    <template v-slot:body>#몸통</template>
    <template #header>#머리</template>
    <template #[slot]>#동적으로!!</template>
    <template v-slot:default>#다리</template>
  </FancyButton>
  <input type="text" v-model="activeSlot" />
</template>

<script>
import { ref } from 'vue'
import FancyButton from './lectures/FancyButton.vue'

export default {
  components: {
    FancyButton
  },
  setup() {
    const activeSlot = ref('activeSlot')

    return {
      FancyButton,
      activeSlot
    }
  }
}
</script>

<style lang="scss" scoped></style>
