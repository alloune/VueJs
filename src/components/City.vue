<template>
  <div>
    <p>{{ name }}</p>
    <p>{{ weather }}</p>
    <p>{{ temperature }}</p>
    <p>{{ updatedAt }}</p>
  </div>


</template>

<script>

export default {
  name: "CityWeather",
  props: {
    name:String,
    weather:String,
    temperature:Number,
    updatedAt:String,
  }
}
</script>

<style scoped>

</style>