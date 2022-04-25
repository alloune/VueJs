<template>
  <div class="about">

    <CitiesList msg="Bienvenue sur la page d'affichage des infos météo"/>
  </div>
</template>
<script>
import CitiesList from "@/components/CitiesList";

export default {
  name: 'CitiesView',
  components: {
    CitiesList,
  }
}
</script>