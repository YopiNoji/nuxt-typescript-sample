<template>
  <div class="container">
    <h2>{{ state.messageOne }}</h2>
    <h2>{{ messageTwo }}</h2>
    <counter />
  </div>
</template>

<script lang="ts">
import {
  defineComponent,
  reactive,
  ref,
  onMounted,
  onUpdated,
  onUnmounted
} from '@vue/composition-api'
import Counter from '~/components/composition/Counter.vue'

export default defineComponent({
  layout: 'menu',
  components: {
    Counter
  },
  setup() {
    onMounted(() => {
      console.log('mounted!')
    })
    onUpdated(() => {
      console.log('updated!')
    })
    onUnmounted(() => {
      console.log('unmounted!')
    })
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

<style lang="scss">
@import '@/assets/scss/main.scss';
</style>
