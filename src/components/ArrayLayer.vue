<template>
  <div></div>
</template>
<script>

export default {
  name: 'ArrayLayer',
  props: {
    data: {
      type: Array,
      default: () => []
    },
    options: {
      type: Object,
      default: () => {}
    },
    layerOptions: {
      type: Object,
      default: () => {}
    },
  },
  // watch() {
  //   data: {
  //     handler (newData) {
  //       window.console.log("Data changed. newData=" + newData)
  //     }
  //   },
  //   options: {
  //     handler (newOptions) {
  //       window.console.log("Options changed. newOptions=" + newOptions)
  //     },
  //     // deep: true
  //   },
  //   layerOptions: {
  //     handler (newLayerOptions) {
  //       window.console.log("Options changed. newLayerOptions=" + newLayerOptions)
  //     }
  //   }
  // },
  beforeCreate() {
    window.console.log("BEFORE CREATE")
  },
  created() {
    window.console.log("HELLO WORLD - created")
  },
  mounted() {
    window.console.log("HELLO WORLD")
    window.console.log(this.$parent)
    this.layer = this.$parent.plot.overlay_array(
      this.data,
      this.options,
      this.layerOptions
    )
  },

  beforeDestroy () {
    if (this.layer) {
      /* @TODO: do something... */
    }
  }
}
</script>
