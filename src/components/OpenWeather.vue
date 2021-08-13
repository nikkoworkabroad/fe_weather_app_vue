<template>
  <div>
    <div class="row" style="margin-top:40px">
      <div class="col-sm-4"></div>
      <div class="col-sm-8">
        
        <div v-bind:key="weather.where" v-for="weather in weathers ">
          <div style="margin-bottom: 30px; border: 2px solid #212529; width: 300px; padding: 10px">
            <h1><strong>{{weather.where}}</strong></h1>
            <h1>{{weather.temperature}}&deg; <small>{{weather.unit}} </small></h1>
            <h1>{{weather.description}}</h1>
          </div>
      </div>

      </div>
    </div>
 
  </div>
</template>

<script>
export default {
  name: 'OpenWeather',
  components: {
  
  },
  data(){
      return{
          msg: "NIKKO",
       }
  },
  props: ["weathers"]
  

}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
