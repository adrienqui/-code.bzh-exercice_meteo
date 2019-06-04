<template>
  <div id="app">
    <Recherche :appid="appid" @result="setMeteo" />
    {{ meteo }}
  </div>
</template>

<script>
import Recherche from './components/Recherche.vue'

export default {
  name: 'app',
  data: function () {
    return {
      appid: '7ddca0329077061fa15dbc6593241269',
      meteo: null
    }
  },
  components: {
    Recherche
  },
  methods: {
    setMeteo: function(value) {
      this.meteo = value
    }
  }
}
</script>
