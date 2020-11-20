<template>
  <Nav />

  <div class="px-6">
    <section class="max-w-3xl mx-auto mb-12">
    <div class="bg-white lg:flex lg:shadow-lg lg:rounded-lg">
      <div class="p-12 text-center">
        <h2 class="text-2xl text-gray-800 font-bold md:text-3xl">Laravel Developer in Hamilton, Ontario.</h2>
        <p class="mt-4 text-gray-500">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Autem ab neque, pariatur voluptatibus officia quas! Exercitationem, sed ipsa odio aperiam temporibus architecto eos? Minus sint accusamus architecto tempore, beatae reiciendis?</p>

        <div class="mt-8">
          <a href="#" class="bg-gray-900 text-gray-100 px-5 py-3 font-semibold rounded hover:bg-gray-800 hover:shadow-lg">Start Now</a>
        </div>
      </div>
    </div>
  </section>
  </div>

  <BlogPost />
  <BlogPost />
  <BlogPost />
  <BlogPost />

  <Footer />
</template>

<script>
import Nav from './components/Nav.vue';
import Footer from './components/Footer.vue';
import BlogPost from './components/BlogPost.vue';

export default {
  name: 'App',
  components: { Nav, Footer, BlogPost },
  setup() {}
}
</script>
