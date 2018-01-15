<script>
import Mouse from '@/components/Mouse'
import Child from '@/components/Child'

export default {
  components: {
    Mouse,
    Child,
  },

  render () {
    return (
      <div id='app'>
        <Mouse
          scopedSlots={{ default: this.renderChild.bind(this, 'ScopedSlot') }}
          render={this.renderChild.bind(this, 'RenderProp')} />
      </div>
    )
  },

  methods: {
    renderChild (source, mouse) {
      return <Child source={source} x={mouse.x} y={mouse.y} />
    },
  },
}
</script>

<style>
html, body {
  height: 50%;
}

#app {
  height: 100%;
}
</style>
