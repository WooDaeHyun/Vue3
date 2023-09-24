<template>
  <div>
    <button @click="printEvent('메세지', $event)">inline event info</button>
  </div>
</template>

<script>
export default {
  setup() {
    const printEvent = (message, event) => {
      console.log('message', message)
      console.log('evnetTarget', event.target)
      console.log('eventTargetTagname', event.target.tagName)
    }

    return { printEvent }
  }
}
</script>

<style lang="scss" scoped></style>
