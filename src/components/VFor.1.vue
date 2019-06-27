<template>
  <div>
    {{ list[0] }}
    <v-for v-if="list.length > 1" :list="list.slice(1)" />
  </div>
</template>

<script>
export default {
  name: 'VFor',

  props: {
    list: {
      type: Array,
      required: true,
    }
  }
}
</script>
