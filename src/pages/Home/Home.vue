<template>
  <div style="height:100%;width:100%;">
    <Banner />
    <Content />
    <Source />
    <Contact />
    <Footer />
  </div>
</template>

<script>
import Banner from '../../components/Banner/Banner.vue';
import Content from '../../components/Content/Content.vue';
import Source from '../../components/Source/Source.vue';
import Contact from '../../components/Contact/Contact.vue';
import Footer from '../../components/Footer/Footer.vue';

export default {
  components: {
    Banner,
    Content,
    Source,
    Contact,
    Footer,
  },
};
</script>

<style>
</style>