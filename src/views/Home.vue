<template>
  <div>
    <Header />
    <!-- Home Description -->
    <section id="home-title">
      <div class="flex justify-center mt-24 md:mt-48 lg:mt-64 xl:mt-36">
        <div class="text-white">
          <h1 class="text-4xl font-bold text-center">Join us today</h1>
          <p class="text-sm md:text-lg md:max-w-md md:text-center mx-4 md:mx-0 lg:mx-0 mt-2.5">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Dignissimos
            laudantium fugit voluptatibus repellat, inventore totam!
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
export default {
  components: {
    HomeContent,
    LoginButton,
    Login
  },
};
</script>

<style>
</style>