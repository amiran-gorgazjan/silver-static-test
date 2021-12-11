<template>
  <div class="container mt-5">
    <nav>
      <ul class="list">
        <li class="link"><router-link to="/">Home</router-link></li>
        <li class="link"><router-link to="/resume">Resume</router-link></li>
        <li class="link"><router-link to="/bio">Bio</router-link></li>
        <li class="link"><router-link to="/blog">Blog</router-link></li>
        <li class="link"><router-link to="/contact">Contact</router-link></li>
      </ul>
    </nav>

    <Nuxt />
  </div>

</template>

<style lang="scss" scoped>
  .list {
    list-style-type: none;
    margin: 0;
    padding: 0;
    margin-bottom: 2rem;
  }

  .link {
    display: inline-block;
    margin: 0;
    padding: 0;
    margin-right: 1rem;
  }
</style>
