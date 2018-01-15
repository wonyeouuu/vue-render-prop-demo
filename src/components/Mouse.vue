<script>
export default {
  render () {
    return (
      <div
        class='mouse-container'
        on-mousemove={this.handleMouseMove}>
        <pre>(Mouse Component)Current coordinate is: ({this.x}, {this.y})</pre>
        {this.$props.render(this.$data)}
        {this.$scopedSlots.default(this.$data)}
      </div>
    )
  },

  props: {
    render: Function,
  },

  data () {
    return {
      x: 0,
      y: 0,
    }
  },

  methods: {
    handleMouseMove (e) {
      this.x = e.clientX
      this.y = e.clientY
    },
  },
}
</script>

<style>
.mouse-container {
  border: 1px solid black;
  height: 100%;
  padding: 10px;
}
</style>
