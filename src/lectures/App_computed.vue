<template>
  <div>
    <h2>{{ teacher.name }}</h2>
    <h3>강의가 있습니까?</h3>
    <p>{{ hasLecture }}</p>
    <h2>name</h2>
    <div>{{ fullName }}</div>
  </div>
</template>

<script>
import { reactive, computed, ref } from 'vue'

export default {
  setup() {
    const teacher = reactive({
      name: '짐코딩',
      lectures: ['html/css', 'javascript', 'vue3']
    })

    const hasLecture = computed(() => {
      return teacher.lectures.length > 0 ? '있음!!' : '없음'
    })

    const firstName = ref('홍')
    const lastName = ref('길동')
    const fullName = computed(() => firstName.value + ' ' + lastName.value)

    return {
      teacher,
      hasLecture,
      firstName,
      lastName,
      fullName
    }
  }
}
</script>

<style lang="scss" scoped></style>
