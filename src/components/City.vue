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
    updatedAt:Number,
    icone:String

  },
  methods:{
    stringToDate(timestamp){

      let date = new Date(timestamp * 1000);
      // let months = ['Jan','Feb','Mar','Apr','May','Jun','Jul','Aug','Sep','Oct','Nov','Dec'];
      // let year = date.getFullYear();
      // let month = months[date.getMonth()];
      // let date1 = date.getDate();
      // let hour = date.getHours();
      // let min = date.getMinutes();
      // let sec = date.getSeconds();
      // let time = date1 + ' ' + month + ' ' + year + ' ' + hour + ':' + min + ':' + sec ;
      return date;

    }
  },
  computed:{
    formatedDate: function () {
      return format(this.stringToDate(this.updatedAt))
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