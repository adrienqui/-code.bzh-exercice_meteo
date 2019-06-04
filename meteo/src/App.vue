<template>
  <div id="app">
    <Recherche :appid="appid" @result="setMeteo" />
    <Meteo v-if="meteo" :meteo="meteo" />
  </div>
</template>

<script>
import Recherche from './components/Recherche.vue'
import Meteo from './components/Meteo.vue'

export default {
  name: 'app',
  data: function () {
    return {
      appid: '7ddca0329077061fa15dbc6593241269',
      meteo: null
    }
  },
  components: {
    Recherche,
    Meteo
  },
  methods: {
    setMeteo: function(value) {
      this.meteo = value
    }
  }
}
</script>
