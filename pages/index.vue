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

    <section id="/" class="max-w-md mx-auto bg-purple-100 rounded-xl shadow-md overflow-hidden md:max-w-xl">
      <div class="md:flex">
        <h1 class="font-extrabold mt-6 mb-6 ml-10 text-gray-500 text-2xl tracking-wide">Greetings! Good day!</h1>
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
