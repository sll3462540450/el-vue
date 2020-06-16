<template>
  <div>
    <Header />
    <Content />
    <Gategory />
    <Footer />
  </div>
</template>

<script>
import Header from "./Home/Header";
import Content from "./Home/Content";
import Gategory from "./Home/Gategory";
import Footer from "./Home/Footer";
export default {
  components: {
    Header,
    Content,
    Gategory,
    Footer
  }
};
</script>

<style>
</style>