<template>
  <div id="app">
   
    <!-- <TremendousWeather v-bind:weathers="weathers"></TremendousWeather> -->
     <div class="row" style="margin-top:40px">
      <div class="col-sm-4"></div>
      <div class="col-sm-8">
        
        <div style="margin-bottom: 30px; border: 2px solid #212529; width: 300px; padding: 10px">
            <h1><strong>{{where}}</strong></h1>
            <h1>{{temperature}}&deg; <small>{{unit}} </small></h1>
            <h1>{{description}}</h1>
          </div>
   

        </div>

      </div>

</div>
</template>

<script>

// import TremendousWeather from '../components/TremendousWeather.vue';
import axios from 'axios';

export default {
  name: 'App',
  components: {
    // TremendousWeather,
  },
  data(){
    return {
      where: "",
      temperature :"",
      unit : "",
      description: "",
    }
  },
  created()
  {
   
  var vm = this;
			axios.get("api/weather1.json")
				.then(function (response) {
				console.log(   response.data)
        vm.where = response.data.name;
        vm.temperature = response.data.main.temp.value;
        vm.unit = response.data.main.temp.unit;
        vm.description = response.data.service.name;
      })
  }
}
</script>

<style>

</style>
