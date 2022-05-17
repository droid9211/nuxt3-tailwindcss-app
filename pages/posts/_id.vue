<template>
  <NuxtLayout>
    <header>
      <nav class="nav bg-gray-100 shadow-xl">
        <ul class="flex space-x-2 p-4 rounded-md text-xl bg-amber-100 text-amber-700 font-semibold">
          <nuxt-link to="/" tag="li"><a>Home</a></nuxt-link>
          <nuxt-link to="/posts" tag="li"><a>Posts</a></nuxt-link>
        </ul>
      </nav>
    </header>

    <section id="/post/_id"
      class="max-w-md m-36 p-8 mx-auto bg-indigo-50 rounded-xl shadow-md overflow-hidden md:max-w-xl">
      <div class="md:block">
        <p v-if="$fetchState.pending">Loading....</p>
        <p v-else-if="$fetchState.error">Error while fetching posts</p>
        <h1 class="font-extrabold mb-6 text-gray-700 text-2xl tracking-wide">{{ post.title }}</h1>
        <p class="text-left text-base">{{ post.body }}</p>
      </div>
      <nuxt-link to="/posts" tag="li" class="back mt-6 font-medium"><a>Back to Posts</a></nuxt-link>
    </section>

    <footer class="main-footer font-sans bg-gray-100 shadow-inner">
      <div>
        <p> © 2022 – Made by Lilly A. Nikolova</p>
      </div>
    </footer>
  </NuxtLayout>
</template>

<script>
export default {
  data() {
    return {
      post: []
    }
  },
  async fetch() {
    this.post = await fetch(
      `https://jsonplaceholder.typicode.com/posts/${this.$route.params.id}`
    ).then(res => res.json())
  }
}
</script>

<style>
.back {
  list-style: none;
}
</style>