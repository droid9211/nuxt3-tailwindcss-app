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

    <section id="/" class="mt-6 p-8">
      <div class="md:block pl-6 mb-6 max-w-4xl mx-auto bg-indigo-100 rounded-l shadow-md overflow-hidden md:max-w-xxl bg-amber-50 text-amber-700 mb-6">
        <h1 class="text-center font-extrabold mt-6 mb-6 text-gray-700 text-2xl tracking-wide">Greetings! Good day!</h1>
        <p class="p-8 mb-6">Here are the steps which I've made in building the current blog-type app: <br>
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
.nav ul {
  text-align: center;
  justify-content: space-evenly;
}

a:hover {
  color: rgb(52, 174, 235);
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
