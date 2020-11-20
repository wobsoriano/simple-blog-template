<template>
    <footer class="flex justify-center px-4 text-gray-100 bg-gray-800">
        <div class="container py-6 max-w-3xl">
            <h1 class="text-center text-lg font-bold lg:text-2xl">
                Join 31,000+ other and never miss <br> out on new tips, tutorials, and more.
            </h1>

            <div class="flex justify-center mt-6">
                <div class="bg-white rounded-md">
                    <div class="flex flex-wrap justify-between md:flex-row">
                        <input type="email" class="m-1 p-2 appearance-none text-gray-700 text-sm focus:outline-none focus:placeholder-transparent" placeholder="Enter your email" aria-label="Enter your email" />
                        <button class="w-full m-1 p-2 text-sm bg-gray-800 rounded font-semibold uppercase lg:w-auto hover:bg-gray-700">subscribe</button>
                    </div>
                </div>
            </div>

            <hr class="h-px mt-6 bg-gray-700 border-none" />

            <div class="flex flex-col items-center justify-between mt-6 md:flex-row">
                <div>
                    <a href="#" class="text-xl font-bold text-gray-100 hover:text-gray-300">David Grzyb</a>
                </div>

                <div class="flex mt-4 md:m-0">
                    <div class="-mx-4">
                        <a v-for="link in links" :key="link" href="#" class="px-4 text-sm text-gray-100 font-medium hover:text-gray-300">{{ link }}</a>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'Footer',
  setup() {
    const links = ref([
      'Home',
      'About',
      'Contact'
    ]);

    return { links }
  }
}
</script>
