<script>
export default {
  name: 'VIf',

  props: {
    condition: {
      type: Boolean,
      required: true,
    }
  },

  render(h) {
    return this.condition
      ? this.$slots.default
      : null;
  }
}
</script>
