<template>
  <div>
    <h1>Blog</h1>

    <p>This is a blog built with Vue.js, Nuxt and @nuxt/content and hosted on Github Pages.</p>

    <nav>
      <ul>
        <li v-for="post in posts" :key="post.slug">
          <nuxt-link :to="`/blog/${post.slug}`">
            {{ post.title || post.slug }}
          </nuxt-link>
          {{ post.createdAt }}
        </li>
      </ul>
    </nav>
  </div>
</template>
<script>
export default {
  async asyncData ({ $content, params }) {
    const posts = await $content('posts').sortBy('createdAt', 'desc').fetch()
    console.log(posts)
    return { posts }
  },
  data () {
    return {
      posts: []
    }
  }
}
</script>
