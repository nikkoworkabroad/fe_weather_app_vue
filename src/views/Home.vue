<template>
  <div id="app">
    <OpenWeather v-bind:weathers="weathers"></OpenWeather>
  
</div>
</template>

<script>

import OpenWeather from '../components/OpenWeather.vue';
import axios from 'axios';

export default {
  name: 'App',
  components: {
   OpenWeather,

  },
  data(){
    return {
      name: "Nikko Zabala",
      weathers :[],
 
    }
  },
  created()
  {
    axios.get('api/weather0.json')
    .then(res => this.weathers = res.data);
  
  }
}
</script>

<style>

</style>
