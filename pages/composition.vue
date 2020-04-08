<template>
  <div class="container">
    <h2>{{ state.messageOne }}</h2>
    <h2>{{ messageTwo }}</h2>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref } from '@vue/composition-api'

export default defineComponent({
  layout: 'menu',
  setup() {
    const state = reactive<{ messageOne: string }>({
      messageOne: 'Hello'
    })
    const messageTwo = ref<string>('こんにちは')

    return {
      state,
      messageTwo
    }
  }
})
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
