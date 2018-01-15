<script>
export default {
  render () {
    return (
      <div class='child-container'>
        <pre>({this.source})Current coordinate is: ({this.$props.x}, {this.$props.y})</pre>
      </div>
    )
  },

  props: {
    x: Number,
    y: Number,
    source: String,
  },
}
</script>

<style>
.child-container {
  border: 1px solid red;
  margin-bottom: 5px;
}
</style>
