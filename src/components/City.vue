<template>
  <div>
    <h2>{{ name }}</h2>
    <p>Météo : {{ weather }}</p>
    <p>Température : {{ temperature }} °C</p>
    <p>Dernière mise à jour: {{ formatedDate }}</p>
  </div>


</template>

<script>
import { format } from 'timeago.js';
export default {
  name: "CityWeather",
  props: {
    name:String,
    weather:String,
    temperature:Number,
    updatedAt:Date,
  },
  computed:{
    formatedDate: function () {
      return format(this.updatedAt, 'fr_FR', {relativeDate:"2022-4-26"})
    }
  }
}
</script>

<style scoped>
div{
  border:2px solid black;
  display:flex;
  flex-direction:column;
  align-items: flex-start;
  padding: 15px;
  border-radius: 15px;
  background-color: ghostwhite;
}
</style>