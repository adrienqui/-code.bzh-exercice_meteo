<template>
  <div>
    <p>Météo de la ville de {{ meteo.city.name }} (population : {{ meteo.city.population }} habitants)</p>
    <hr/>
    <ul>
      <li
        v-for="(prevision, index) of meteo.list"
        :key="index">
        [{{ prevision.dt_txt }}] => {{ prevision.main.temp }}°C, humidité {{ prevision.main.humidity }}%, {{ prevision.weather[0].description }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Meteo',
  props: {
    meteo: Object
  }
}
</script>
