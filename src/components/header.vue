<template lang="html">
  <div id="header">
    <p>
      <button type="button" name="button" @click="sendMessage">向Footer组件发送数据</button>
    </p>
  </div>
</template>

<script>
  import {EventBus} from './../event-bus.js';
  export default {
    components: {

    },
    data () {
      return {
        msg: '我是来自Header组件的数据'
      };
    },
    methods: {
      sendMessage () {
        // console.log(EventBus);
        EventBus.$emit('messageSent',this.msg);
      }
    }
  }
</script>

<style lang="css">
</style>
