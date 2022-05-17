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

     <section id="/posts" class="mt-6 p-6"> 
            <div class="p-8  bg-indigo-50 rounded-xl shadow-md md:block max-w-3xl mx-auto md:max-w-xxl mb-6">
                <h1 class="text-center font-extrabold mb-6 text-gray-700 text-2xl tracking-wide">Posts:</h1>
                    <p v-if="$fetchState.pending">Loading....</p>
                    <p v-else-if="$fetchState.error">Error while fetching posts</p>
                    <ul v-else>
                        <li v-for="(post, index) in posts" :key="index"
                            class="block mt-3 p-2 text-lg leading-loose font-sans text-black">
                            <NuxtLink v-bind:to="'/posts/' + post.id" class="text-center p-4 mb-2 bg-white rounded-xl shadow-md text-amber-700">
                                {{ post.id }} . {{ post.title }}</NuxtLink>
                        </li>
                    </ul>
            </div>
        </section> -->

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
            posts: []
        }
    },
    async fetch() {
        this.posts = await fetch(
            'https://jsonplaceholder.typicode.com/posts/'
        ).then(res => res.json())
    }
}
</script>
