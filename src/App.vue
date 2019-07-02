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

    <p>
      <v-if :condition="false">
        First condition is true
        <template #false>
          <v-if :condition="true">
            Second condition is true
          </v-if>
        </template>
      </v-if>
    </p>
  </div>
</template>

<script>
import VFor from './components/VFor';
import VIf from './components/VIf';

export default {
  name: 'app',

  components: {
    VFor,
    VIf,
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
