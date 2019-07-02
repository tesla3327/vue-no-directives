<template>
  <v-nodes
    :v-nodes="condition
      ? $slots.default
      : null"
  />
</template>

<script>
import VNodes from './VNodes';

export default {
  name: 'VIf',

  components: {
    VNodes,
  },

  props: {
    condition: {
      type: Boolean,
      required: true,
    }
  },
}
</script>
