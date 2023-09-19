<template>
  <div>
    <!-- 인라인 방식 -->
    <div class="text" :class="{ active: isActive, 'text-danger': hasError }">텍스트!</div>
    <!-- boolean 값을 통해서 class를 사용할지 말지 선택할 수 있음!! -->
    <hr />
    <!-- 만약 바인딩할 데이터가 많다면 인라인이 아닌 object로 바인딩할 수도 있음 -->
    <div class="text" :class="classObject">텍스트!</div>
    <!-- 배열로 클래스를 넣을 수도 있음!!  -->
    <div class="text" :class="[isActive ? 'active-class' : 'class', errorClass, classObject]">
      <!-- 배열안에 삼항연산자도 사용가능하고 객체도 넣을 수 있다.. 짬뽕임 -->
      텍스트!
    </div>
    <button @click="changeStyle">스타일 변경</button>
  </div>
</template>

<script>
import { computed, ref } from 'vue'

export default {
  setup() {
    const isActive = ref(true)
    const hasError = ref(true)

    const changeStyle = () => {
      isActive.value = !isActive.value
      hasError.value = !hasError.value
    }

    const classObject = ref({
      active: isActive.value,
      'text-danger': false
    })

    // const classObject = computed(() => {
    //   return {
    //     active: isActive.value,
    //     'text-danger': hasError.value
    //   }
    // })

    const activeClass = ref('active')
    const errorClass = ref('error')

    return {
      isActive,
      changeStyle,
      hasError,
      classObject,
      activeClass,
      errorClass
    }
  }
}
</script>

<style lang="scss" scoped>
.active {
  color: red;
}

.text {
  text-decoration-line: line-through;
}

.text-danger {
  font-weight: 900;
}
</style>
