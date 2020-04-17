<template>
  <div>
    <button @click="increment">Increment ++</button>
    <p>{{ count }}</p>
  </div>
</template>

<script lang="ts">
import { createComponent, ref } from '@vue/composition-api'

// カウンターに関わるものを関数でまとめる
const useCounter = () => {
  const count = ref(0)
  const increment = () => {
    count.value++
  }
  return { count, increment }
}

export default createComponent({
  setup() {
    const { count, increment } = useCounter()
    return { count, increment }
  }
})
</script>

<style lang="scss">
@import '@/assets/scss/main.scss';
</style>
