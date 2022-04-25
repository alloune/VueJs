<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <li v-for="city in info.data.list" :key="city.id">
            <CityWeather :name="city.name" :weather="city.weather[0].description" :temperature="city.main.temp"
                   :updatedAt="city.dt" :icone="city.weather[0].icon"/>
    </li>

  </div>
</template>

<script>

const axios = require('axios').default;

import CityWeather from "@/components/City";

export default {
  name: 'CitiesList',
  components: {CityWeather},
  props: {
    msg: String,
  },
  data() {
    return {
      info: null
    }
  },
  mounted() {
    axios.get('https://api.openweathermap.org/data/2.5/find?lat=45.188&lon=5.724&cnt=20&cluster=yes&lang=fr&units=metric&APPID=0506069a027cb95323bf9f08f15feb11').then(response => this.info = response)
  }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
