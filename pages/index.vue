<template>
  <div>
    <h1 class="main-title">
      Hello World 1
    </h1>
    <p>This is a simple example of a Vue.js component. <span class="my-message">{{ message }}</span></p>
    <p>
      <button class="btn btn-primary" @click="changeMessage">
        Change Message
      </button>
    </p>

    <Calculator />
  </div>
</template>

<script>
import Calculator from '~/components/Calculator.vue'

export default {
  components: {
    Calculator
  },
  data () {
    return {
      message: 'Hello Vue!'
    }
  },
  methods: {
    changeMessage () {
      this.message = 'Hello Silver!'
    }
  }
}
</script>

<style lang="scss" scoped>
.my-message {
  color: red;
}
</style>
