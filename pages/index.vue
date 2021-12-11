<template>
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <nav>
          <nuxt-link to="/blog">
            My Blog
          </nuxt-link>
        </nav>

        <h1 class="main-title">
          Hello World 1
        </h1>
        <p>This is a simple example of a Vue.js component. <span class="my-message">{{ message }}</span></p>
        <p>
          <button class="btn btn-primary" @click="changeMessage">
            Change Message
          </button>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
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

<style lang="scss">
.container {
  margin-top: 80px;
}
.my-message {
  color: red;
}
</style>
