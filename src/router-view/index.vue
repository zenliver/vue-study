<template>
  <div id="router-view">
    <h1>首页</h1>
    <p>
      <button type="button" name="button" @click="callFooterAlert">执行Footer中的alert</button>
    </p>
    <Footer ref="footer" :prop1="prop1"></Footer>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
  import Footer from './../components/footer.vue';

  export default {
    name: 'index',
    components: {
      Footer
    },
    data() {
      return {
        prop1: 'prop1'
      };
    },
    methods: {
      callFooterAlert() {
        this.prop1 = 'prop1_modified';
        // this.$refs.footer.Alert();
        console.log(this.$refs.footer.msgFromHeader);
        console.log(this.$refs.footer.clickCount);
        console.log(this.$refs.footer.prop1);
      },
    },
  }
</script>
