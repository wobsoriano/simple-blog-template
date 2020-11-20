<template>
  <nav class="bg-white shadow mb-10">
    <div class="max-w-3xl mx-auto py-3 px-6 md:px-0 md:flex md:justify-between md:items-center">
      <div class="flex justify-between items-center">
        <div class="flex items-center">
          <img src="https://davidgrzyb.com/storage/david-grzyb.jpg" class="h-8 shadow rounded-full" alt="profile" />
          <a href="#" class="text-gray-800 text-xl hover:text-gray-700 ml-4">David Grzyb</a>
        </div>
        <!-- Mobile menu button -->
        <div class="flex md:hidden">
          <button @click="isOpen = !isOpen" type="button" class="text-gray-500 hover:text-gray-600 focus:outline-none focus:text-gray-600" aria-label="toggle menu">
            <svg viewBox="0 0 24 24" class="h-6 w-6 fill-current">
              <path fill-rule="evenodd" d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"></path>
            </svg>
          </button>
        </div> 
      </div>

      <!-- Menu, if mobile set to hidden -->
      <div :class="`${isOpen ? 'show' : 'hidden'} md:flex items-center md:block mt-4 md:mt-0`">
        <div class="flex flex-col md:flex-row md:ml-6">
          <a v-for="link in links" :key="link" href="#" class="my-1 text-sm text-gray-700 font-medium hover:text-indigo-500 md:mx-4 md:my-0">{{ link }}</a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'Nav',
  setup() {
    const links = ref([
      'Home',
      'About',
      'Contact'
    ]);
    const isOpen = ref(false);

    return { links, isOpen }
  }
}
</script>
