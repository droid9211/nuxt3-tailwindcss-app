<template>
    <NuxtLayout>
        <header>
            <nav class="font-sans bg-gray-100 shadow-inner font-normal">
                <ul class="nav-links">
                    <nuxt-link to="/" tag="li"><a>Home</a></nuxt-link>
                    <nuxt-link to="/posts" tag="li"><a>Posts</a></nuxt-link>
                </ul>
            </nav>
        </header>

        <section id="/posts" class="max-w-md mx-auto bg-purple-100 rounded-xl shadow-md overflow-hidden md:max-w-3xl">
            <h1 class="font-extrabold mt-6 text-gray-500 text-2xl tracking-wide">Posts:</h1>
            <div class="md:flex">
                <!-- <NuxtChild :key="$route.params.id" /> -->
                <p v-if="$fetchState.pending">Loading....</p>
                <p v-else-if="$fetchState.error">Error while fetching posts</p>
                <ul v-else class="p-8">
                    <li v-for="(post, index) in posts" :key="index"
                        class="block mt-3 p-2 text-lg font-normal leading-loose font-sans text-black">
                        <NuxtLink v-bind:to="'/posts/' + post.id" class="p-2 rounded-md shadow-xl text-slate-500">
                            {{ post.id }} . {{ post.title }}</NuxtLink>
                    </li>
                </ul>
            </div>
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

<style>
h1 {
    text-align: center;
}

.main-footer {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 5%;
}

.main-footer p {
    display: block;
    margin: 0 auto;
    font-size: small;
    padding: 0.7rem;
    text-align: center;
}
</style>