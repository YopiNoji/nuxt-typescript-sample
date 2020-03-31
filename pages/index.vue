<template>
  <div class="container">
    <div>
      <logo />
      <p@click="increment">TEST<p/>
      <input type="text" placeholder="ID" />
      <input type="password" placeholder="PASSWORD" />
      <button type="submit">SUBMIT</button>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Logo from '@/components/index/Logo.vue'
// Only Options API

export default Vue.extend({
  components: {
    Logo
  },
  data() {
    return {
      number: 99
    }
  },
  computed: {
    num(): Number {
      return this.number + 1
    }
  },
  methods: {
    increment(): void {
      console.log(this.num)
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
