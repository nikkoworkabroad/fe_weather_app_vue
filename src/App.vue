<template>
  <div id="app">
    <Header></Header>
    <router-view/>
  </div>
</template>

<script>
import Header from './components/layout/Header.vue';
export default {
  name: 'App',
  components: {
    Header
    },
  
}

</script>

<style>

  ul {list-style-type: none;
		}
 
	body {font-family: 'Open Sans', sans-serif;}
</style>
