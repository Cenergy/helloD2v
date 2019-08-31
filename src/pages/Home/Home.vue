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
import $ from 'jquery';

window.$ = window.jquery = window.jQuery = $;

import { WOW } from 'wowjs';
window.WOW = WOW;

import '../../../static/js/owl';
import 'bootstrap';
import 'stickUp/build/js/stickUp';
import 'classie';
import 'jquery-migrate/dist/jquery-migrate';
import 'imports-loader?this=>window!../../../static/js/modernizr';
import '../../../static/js/jquery.magnific-popup.js';
import '../../../static/js/uiMorphingButton_inflow.js';

console.log('Go: WoW', WOW);
export default {
  mounted() {
    jQuery(function($) {
      $(document).ready(function() {
        $('.navbar-default').stickUp();
      });
    });
    new WOW().init();
    this.loadJsScript('./static/js/script.js');
    // // 测试
  },
  methods: {
    loadJsScript(url) {
      var script = document.createElement('script');
      script.type = 'text/javascript';
      script.src = url;
      const head = document.getElementsByTagName('head')[0];
      head.appendChild(script);
    },
  },
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