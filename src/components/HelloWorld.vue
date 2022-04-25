<template>
  <div class="hello">
    <h1>{{msg}}</h1>
    <cityWeather :name="name" :weather="weather" :temperature="temperature" :updated-at="updatedAt"/>
  </div>
</template>

<script>

import CityWeather from "@/components/City";
export default {
  name: 'HelloWorld',
  components: {CityWeather},
  props: {
    msg: String
  },
data(){
  return {
    name: 'Ma ville', // nom de la ville
    weather: 'Peu nuageux', // descriptif météo
    temperature: 20.55, // température en °C
    updatedAt: new Date().toLocaleDateString() ,// date de dernière mise à jour
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
