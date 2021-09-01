<template>
  <header>
      <!-- Logo -->
    <div id="logo" class="hidden md:flex md:justify-center">
      <img  src="../assets/images/logo.svg" alt="logo" class="bg-white px-14 py-3 rounded-bl-3xl rounded-br-3xl"/>
    </div>
    <!-- Desktop & Tablet Nav -->
    <nav id="navbar" class="lg:container lg:mx-auto md:mt-16 xl:mt-10">
      <div class="hidden md:flex md:justify-start">
            <a href="#" class="d-inline-block mx-8 lg:mx-16 xl:mx-10 text-lg text-white font-semibold border-b">HOME</a>
            <a href="#" class="d-inline-block mx-8 lg:mx-16 xl:mx-10 text-lg text-gray-300">ARTICLES</a>
            <a href="#" class="text-lg text-gray-300 mx-8 lg:mx-16 xl:mx-10">AUDIO</a>
      </div>
      <!-- Mobile Nav -->
      <div id="mobile-menu" class="block md:hidden">
        <div class="flex justify-around bg-white p-4 items-center">
           <button v-if="!visibility" @click="ShowMenu"><i class="fas fa-bars fa-lg text-gray-500"></i></button>
           <button v-else @click="ShowMenu"><i class="fas fas fa-chevron-down text-gray-500"></i></button>
            <img src="../assets/images/mobile-logo.svg" alt="mobile-logo" />
            <i class="fas fa-bell fa-lg text-gray-500"></i>
        </div>
        <!-- Mobile Hamburger Menu -->
        <div v-if="visibility" class="bg-white flex flex-col items-center">
          <div id="search-bar" class="relative">
            <div class="absolute inset-y-0 left-0 flex items-center px-2 pointer-events-none">
                <i class="fas fa-search text-gray-400 ml-16"></i>
            </div>
            <input type="text" class="px-7 py-2.5 text-center border rounded-3xl bg-gray-200 mt-8 inline-block mb-8 focus:outline-none" placeholder="Search"/>
          </div>
          <!-- Mobile links -->
            <a href="#" class="inline-block mb-8 text-purple-800 font-semibold">HOME</a>
            <a href="#" class="inline-block mb-8">ARTICLES</a>
            <a href="#" class="inline-block mb-8">AUDIO</a>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
import {ref} from "vue"
export default {
    data() {
        return {
            visibility: ref(false)
        }
    },
    methods: {
        ShowMenu(){
            this.visibility ? this.visibility = false : this.visibility = true
        }
    }
};
</script>

<style scoped>

</style>
