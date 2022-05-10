<template>
  <div class="q-mb-lg">
    <div  style="height:82vh"  v-if="log" class="row justify-center items-center">
      <div>
        <q-btn @click="TheWether">boshlash</q-btn>
      </div>
    </div>
    <div v-if="start">
      <SunnySpringWeather v-if="weather.main == 'undefined' " :weather="weather"/>
      <CloudSpringWeather  :weather="weather"/>
      <RainSpringWeather v-if="weather.main == 'undefined' " :weather="weather"/>
      <SunnyAutomnWeather v-if="weather.main == 'undefined' " :weather="weather"/>
      <CloudAutomnWeather v-if="weather.main == 'undefined' " :weather="weather"/>
      <RainAutomnWeather v-if="weather.main == 'undefined' " :weather="weather"/>
      <SunnyWinterWeather v-if="weather.main == 'undefined' " :weather="weather"/>
      <CloudWintwerWeather v-if="weather.main == 'undefined' " :weather="weather"/>
      <SnowWinterWeather v-if="weather.main == 'undefined' " :weather="weather"/>
    </div>
  </div>
</template>
<script>
import SunnySpringWeather from 'src/components/SunnySpringWeather.vue'
import SunnyAutomnWeather from 'src/components/SunnyAutomnWeather.vue'
import SunnyWinterWeather from 'src/components/SunnyWinterWeather.vue'
import CloudSpringWeather from 'src/components/CloudSpringWeather.vue'
import RainSpringWeather from 'src/components/RainSpringWeather.vue'
import CloudAutomnWeather from '../components/CloudAutomnWeather.vue'
import RainAutomnWeather from '../components/RainAutomnWeather.vue'
import CloudWintwerWeather from 'src/components/CloudWintwerWeather.vue'
import SnowWinterWeather from 'src/components/SnowWinterWeather.vue'
export default {
  components: {
    SunnySpringWeather,
    SunnyAutomnWeather,
    SunnyWinterWeather,
    CloudSpringWeather,
    RainSpringWeather,
    CloudAutomnWeather,
    RainAutomnWeather,
    CloudWintwerWeather,
    SnowWinterWeather,
  },
  data() {
    return {
      api_key:"5de5cd2df8deaed6b1f0656df251ac79",
      url_base:"https://api.openweathermap.org/data/2.5/",
      request:"Fergana",
      log:true,
      start:false,
      weather:""
    }
  },
  methods:{
    TheWether(){
      this.log=false
      this.start=true
      fetch (`${this.url_base}weather?q=${this.request}&units=metric&appID=${this.api_key} `)
        .then(res =>{
          return res.json()
        }) .then(this.setResults)
    },
    setResults(results){
      this.weather=results
    },
  }
}
</script>
<style>

</style>


