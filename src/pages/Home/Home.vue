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
// import 'owl.carousel/dist/assets/owl.carousel.css';

// import * as owl from 'owl.carousel.es6';
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
    // this.loadJsScript('./static/js/uiMorphingButton_inflow.js');
    // this.loadJsScript('./static/js/jquery.magnific-popup.js');
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
    loadCssStyle(cssText) {
      const style = document.createElement('style');
      style.type = 'text/css';
      style.rel = 'stylesheet';
      const head = document.getElementsByTagName('head')[0];
      style.innerHTML = cssText;
      head.appendChild(style);
    },
    loadScriptString(code) {
      var script = document.createElement('script');
      script.type = 'text/javascript';
      try {
        script.appendChild(document.createTextNode(code));
      } catch (ex) {
        script.text = code;
      }
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