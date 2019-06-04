<template>
  <div>
    <form @submit.prevent="recherche">
      <input type="text" v-model="rechercheInput" />
      <input type="submit" :disabled="rechercheInput==''" />
    </form>
  </div>
</template>

<script>
export default {
  name: 'Recherche',
  props: {
    appid: String
  },
  data: function () {
    return {
      rechercheInput: '',
    }
  },
  computed: {
    url: function () {
      return `https://api.openweathermap.org/data/2.5/forecast?q=${this.rechercheInput},fr&units=metric&lang=fr&appid=${this.appid}`
    }
  },
  methods: {
    recherche: function () {
      fetch(this.url)
      .then(response => { return response.json() })
      .then(result => { this.$emit('result', result) })
    }
  }
}
</script>
