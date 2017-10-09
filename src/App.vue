<style lang="scss" scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
h1{
  display: none;
}
</style>

<template>
  <client-tab></client-tab>
</template>

<script>
import ClientTab from '@/pages/ClientTab'
export default {
  name: 'App',
  components:{
    ClientTab
  }
}
</script>

