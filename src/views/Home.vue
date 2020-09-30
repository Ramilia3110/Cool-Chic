<template>
  <div class="home">
    <Hero />
    <Newcollection />
    <Offer />
    <Summer />
    <Hoodies />
    <Contact />
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import Hero from "@/components/Hero.vue";
import Newcollection from "@/components/Newcollection.vue";
import Offer from "@/components/Offer.vue";
import Summer from "@/components/Summer.vue";
import Hoodies from "@/components/Hoodies.vue";
import Contact from "@/components/Contact.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    Hero,
    Newcollection,
    Offer,
    Summer,
    Hoodies,
    Contact,
    Footer,
  },
};
</script>
<style lang="scss">
.container {
  width: 95%;
  margin: 0 auto;
}
.inner-container {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-column-gap: 20px;
}
</style>
