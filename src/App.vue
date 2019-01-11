<template>
  <div id="app">
    <img src="./assets/RW.svg">
    <!-- <HelloWorld/> -->

    <h1>{{ title }}</h1>
    <input type="text" v-model="title">
    <h2>Liste de tâches</h2>
    <ul id="task-list">
      <li v-for="task in tasks">
        <span v-if="task.tache == 'Faire les courses'" style="color:red;">
          {{ task.tache }}
        </span>
        <span v-else v-show="task.display==true">
          {{ task.tache }}
        </span>
      </li>
    </ul>
    <!-- <Test /> -->
  </div>
</template>

<script>
// import Test from './test'
//
// export default {
//   name: 'App',
//   components: {
//     Test
//   }
// }
module.exports = {
  data: function () {
    return {
      title: 'Titre de mon application',
      tasks: [
        { tache: 'Ranger ma chambre', display: true },
        { tache: 'Faire les courses', display: true },
        { tache: 'Apprendre le langage JS', display: true },
        { tache: 'Lire un livre', display: false }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

img {
  max-height: 25%;
  max-width: 10%;
}
</style>
