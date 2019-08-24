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
const jquery = $;

export default {
  mounted() {
    // function loadJsScript(url) {
    //   var script = document.createElement('script');
    //   script.type = 'text/javascript';
    //   script.src = url;
    //   const head = document.getElementsByTagName('head')[0];
    //   head.appendChild(script);
    // }
    // function loadCssStyle(cssText) {
    //   const style = document.createElement('style');
    //   style.type = 'text/css';
    //   style.rel = 'stylesheet';
    //   const head = document.getElementsByTagName('head')[0];
    //   style.innerHTML = cssText;
    //   head.appendChild(style);
    // }
    // function loadScriptString(code) {
    //   var script = document.createElement('script');
    //   script.type = 'text/javascript';
    //   try {
    //     script.appendChild(document.createTextNode(code));
    //   } catch (ex) {
    //     script.text = code;
    //   }
    //   const head = document.getElementsByTagName('head')[0];
    //   head.appendChild(script);
    // }
    // loadJsScript('./static/js/jquery-1.10.2.js');
    // // loadJsScript('./static/js/jquery-1.10.2.js');
    // loadJsScript('./static/js/bootstrap.js');
    // loadJsScript('./static/js/owl.carousel.js');
    // loadJsScript('./static/js/script.js');
    // loadJsScript('./static/js/stickUp.min.js');
    // // 测试
    // var text = `$(($) =>{$(document).ready(()=> {$('.navbar-default').stickUp();});});`;
    // loadScriptString(text);
    // loadJsScript('https://cdn.bootcss.com/modernizr/2.8.3/modernizr.min.js');
    // loadJsScript('./static/js/modernizr-2.6.2.min.js');
    // loadJsScript('./static/js/jquery.corner.js');
    // loadJsScript('./static/js/wow.min.js');
    // var text1 = `new WOW().init();`;
    // loadScriptString(text1);
    // loadJsScript('./static/js/classie.js');
    // loadJsScript('./static/js/uiMorphingButton_inflow.js');
    // loadJsScript('./static/js/jquery.magnific-popup.js');
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