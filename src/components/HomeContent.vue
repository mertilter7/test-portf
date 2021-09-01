<template>
  <div class="container mx-auto md:flex mt-14">
    <div v-for="data in datas" :key="data.id" class="xl:ml-36">
        <div  id="grid-content" class="grid grid-cols-1 xl:grid-cols-4 my-12 md:my-0">
          <div class="flex flex-col text-white items-center">
            <!-- Content -->
            <figure>
               <img :src="data.image" alt="watch" class="inline-block w-16 xl:w-32"/>
            </figure>
            <div class="w-64 text-center">
              <h4 class="text-lg xl:text-lg font-bold mt-3.5">{{data.title}}</h4>
              <p class="text-sm md:text-xs lg:text-base xl:text-lg mt-1">{{data.description}}</p>
            </div>
            <!-- Content -->
          </div>
        </div>
    </div>
  </div>
</template>

<script>
import axios from "axios"
export default {
  data() {
    return {
      datas : {},
      url : "http://localhost:3000/posts"
    }
  },
  async created() {
    await axios.get(this.url)
     .then((response) => (this.datas = response.data))
  }
}
</script>

<style>
</style>