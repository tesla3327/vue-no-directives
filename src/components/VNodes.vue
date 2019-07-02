<script>
// Helper function to render out raw vnodes that we get
export default {
  name: 'VNodes',
  functional: true,
  render: (h, context) => context.props.vNodes,
};
</script>



// https://stackoverflow.com/questions/49352525/can-you-render-vnodes-in-a-vue-template
