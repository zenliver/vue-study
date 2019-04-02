<template>
  <div id="router-view">
    <h1>首页</h1>
    <Footer></Footer>
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
    }
  }
</script>
