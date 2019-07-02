<template>
  <div>
    <slot v-bind:item="list[0]">
      <!-- Default -->
      {{ list[0] }}
    </slot>
    <v-if :condition="list.length > 1">
      <v-for :list="list.slice(1)">
        <!-- Recursively pass down scoped slot -->
        <template v-slot="{ item }">
          <slot v-bind:item="item" />
        </template>
      </v-for>
    </v-if>
  </div>
</template>

<script>
import VIf from './VIf';

export default {
  name: 'VFor',

  components: {
    VIf,
  },

  props: {
    list: {
      type: Array,
      required: true,
    },
  }
}
</script>
