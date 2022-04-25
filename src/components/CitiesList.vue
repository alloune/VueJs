<template>
  <div class="hello">
    <li v-for="city in cities" :key="city.id">
      <CityWeather :name="city.name" :weather="city.weather" :temperature="city.temperature" :updatedAt="city.updatedAt"/>
    </li>

  </div>
</template>

<script>

import CityWeather from "@/components/City";

export default {
  name: 'CitiesList',
  components: {CityWeather},
  props: {

  },
  data() {
    return {
      cities: [
        {
          id: 1,
          name: 'Grenoble',
          weather: 'Ensoleillé',
          temperature: 22.0,
          updatedAt: new Date()
        },
        {
          id: 2,
          name: 'Montpellier',
          weather: 'Peu nuageux',
          temperature: 19.5,
          updatedAt: new Date()
        }
      ]

    }
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
