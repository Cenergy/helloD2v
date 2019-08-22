<template>
  <div>
    <input type="button" value="happy" @click="lang" />
    <input type="button" value="stop" @click="stop" />
    <h4>{{msg}}</h4>
  </div>
</template>

<script>
export default {
  data() {
    return {
      msg: 'hello world',
      intervalID: null,
    };
  },
  methods: {
    lang() {
      if (this.intervalID) return;
      this.intervalID = setInterval(() => {
        const start = this.msg.substring(0, 1);
        const end = this.msg.substring(1);
        this.msg = end + start;
      }, 400);
    },
    stop() {
      clearInterval(this.intervalID);
      this.intervalID = null;
    },
  },
};
</script>

<style>
</style>
