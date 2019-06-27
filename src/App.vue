<template>
  <div id="app">
    <p>
      Regular list:
      <v-for :list="list" />
    </p>

    <p>
      Bolded list:
      <v-for :list="list">
        <template v-slot="{ item }">
          <strong>{{ item }}</strong>
        </template>
      </v-for>
    </p>
  </div>
</template>

<script>
import VFor from './components/VFor';

export default {
  name: 'app',

  components: {
    VFor,
  },

  data() {
    return {
      list: ['one', 'two', 'three', 'four'],
    };
  },
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
</style>
