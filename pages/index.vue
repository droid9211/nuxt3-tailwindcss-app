<template>
  <NuxtLayout>
    <header>
      <nav class="font-sans bg-gray-100 shadow-inner">
        <ul class="nav-links mb-2">
          <nuxt-link to="/" tag="li"><a>Home</a></nuxt-link>
          <nuxt-link to="/posts" tag="li"><a>Posts</a></nuxt-link>
        </ul>
      </nav>
    </header>

    <section id="/" class=" pb-6 max-w-md mx-auto bg-purple-100 rounded-xl shadow-md overflow-hidden md:max-w-xl">
      <div class="md:block mb-6">
        <h1 class="font-extrabold mt-6 mb-6 ml-6 text-gray-500 text-2xl tracking-wide">Greetings! Good day!</h1>
        <p class="p-6 mb-6">Here are the steps which I've made in building the current blog-type app: <br>
          <b>1. / home</b> <br>
          Home page includes 3 components, which are shared with all the other pages: <br>
          - Header with Navigation <br>
          - Content <br>
          - Footer <br>
          <b>2. / posts</b> <br>
          - Made the posts lists by using the provided REST API from https://jsonplaceholder.typicode.com/posts/ <br>
          - The list is visible on the page <br>
          - Every post is linked to single-post-page ./{id} following the instructions below <br>
          <b>3. / posts / {id}</b> <br>
          - Took the post items from https://jsonplaceholder.typicode.com/posts/ <br>
          - Show post items based on the ID in the URL of application <br>
          - Every post is formated in the provided styling framework. <br>
          <b>From requirements:</b> <br>
          1. Frameworks used for building the application: <br>
          - Nuxt3 <br>
          - Tailwindcss <br>
          2. Functionalities: <br>
          - User is able to see the home page and browse through the navigation to both pages <br>
          - The app has SSR version <br>
          - The app has repository in Github with descriptive changes through each push request <br>
          - Good component separation <br>
          - Good code markup structure and indentation
        </p>
      </div>
    </section>

    <footer class="main-footer font-sans bg-gray-100 shadow-inner">
      <div>
        <p> © 2022 – Made by Lilly A. Nikolova</p>
      </div>
    </footer>
  </NuxtLayout>
</template>

<style>
.nav-links {
  list-style: none;
  margin: 0;
  margin-bottom: 2rem;
  padding: 0.5rem;
  display: flex;
  justify-content: center;
  justify-content: space-evenly;
  align-items: center;
}

.nav-links a:hover {
  color: rgb(122, 83, 231);
}
</style>
