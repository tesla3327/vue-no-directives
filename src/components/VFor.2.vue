<template>
  <div>
    <slot v-bind:item="list[0]">
      <!-- Default -->
      {{ list[0] }}
    </slot>
    <v-for
      v-if="list.length > 1"
      :list="list.slice(1)"
    >
      <!-- Recursively pass down scoped slot -->
      <template v-slot="{ item }">
        <slot v-bind:item="item" />
      </template>
    </v-for>
  </div>
</template>

<script>
export default {
  name: 'VFor',

  props: {
    list: {
      type: Array,
      required: true,
    },
  }
}
</script>
