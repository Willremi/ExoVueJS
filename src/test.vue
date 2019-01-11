<template>
  <div id="app">
    <h1>Bienvenu {{ firstname }}</h1>
    <p>Tu as réussi à diffuser le message</p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      firstname: 'Rémi',
      lastname: 'Willebrouck'
    }
  },
  computed: {
    fullname: function () {
      return this.firstname + ' ' + this.lastname
    }
  }
}
</script>

<style scoped>
h1, h2 {
  font-weight: normal;
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
