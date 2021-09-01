<template>
  <div>
    <!-- Home Description -->
    <section id="home-title">
      <div class="flex justify-center mt-24 md:mt-48 lg:mt-64 xl:mt-42">
        <div v-for="(comment , i) in comments" :key="i" class="text-white  mx-4 md:mx-0 lg:mx-0">
            <h1 class="text-4xl font-bold md:text-center">{{comment.title}}</h1>
            <p class="text-sm md:text-lg md:max-w-xl md:text-center mt-2.5">
              {{comment.description}}
             </p>
        </div>
      </div>
    </section>
    <!-- Home Content -->
    <section id="home-content">
      <home-content />
    </section>
    <!-- Buttons -->
    <section id="home-buttons">
      <login-button />
    </section>
    <!-- Mobile Login Component -->
    <section id="mobile-login">
      <Login />
    </section>
  </div>
</template>

<script>
import HomeContent from "../components/HomeContent.vue";
import LoginButton from "../components/LoginButton.vue";
import Login from "../components/Login.vue"
import axios from "axios"
export default {
  components: {
    HomeContent,
    LoginButton,
    Login
  },
  data() {
    return {
      comments: {},
      url : "http://localhost:3000/comments"
    }
  },
   async created() {
    await axios.get(this.url)
     .then((response) => (this.comments = response.data))
  }
};
</script>
<style>
</style>