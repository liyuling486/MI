<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
  export default {
    name: 'App'
  }
</script>

<style>
  #app {
  }
body{
  padding: 0;
  margin: 0;
}
  * {
    -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
    -webkit-tap-highlight-color: transparent;
  }

  ::-webkit-scrollbar {
    width: 0;
    height: 0;
  }

</style>
