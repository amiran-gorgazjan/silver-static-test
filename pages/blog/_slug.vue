<template>
  <div>
    <h1>{{ post.title || post.slug }}</h1>
    <p class="author">
      {{ post.author }} @ {{ post.createdAt }}
    </p>
    <div class="content">
      <nuxt-content :document="post" />
    </div>

    <h2 class="mt-5">Comments</h2>
    <div id="fb-root" />
    <script async defer crossorigin="anonymous" src="https://connect.facebook.net/en_US/sdk.js#xfbml=1&version=v12.0&appId=3373496136085317&autoLogAppEvents=1" nonce="Ufivddye" />
    <div class="fb-comments" :data-href="`https://https://amiran-gorgazjan.github.io/silver-static-test/blog/${post.slug}`" data-width="" data-numposts="5" />
  </div>
</template>
<script>
export default {
  async asyncData ({ $content, params }) {
    const post = await $content(`posts/${params.slug}`).fetch()
    return { post }
  },

  data () {
    return {
      post: {}
    }
  }
}
</script>
<style lang="scss" scoped>
.author {
  font-size: 0.8em;
  color: #999;
}
</style>
