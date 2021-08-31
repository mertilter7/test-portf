<template>
    <Header />
    <Home />
    <Footer />
</template>

<script>
import Header from "../src/components/Header.vue";
import Home from "./views/Home.vue";
import Footer from "../src/components/Footer.vue"
export default {
  components: {
    Home,
    Header,
    Footer,
  },
};
</script>

<style>
</style>