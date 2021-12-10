<template>
  <div class="blog-container">
    <div class="blog-header">
      <h1>Blog</h1>
    </div>
    <div class="blog-content">
      <div class="blog-post">
        <h2>{{ post.title }}</h2>
        <p>{{ post.content }}</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      post: {
        title: 'My first blog post',
        content: 'This is my first blog post. I hope you like it.'
      }
    }
  }
}
</script>
