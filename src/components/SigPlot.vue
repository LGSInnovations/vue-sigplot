<template>
  <div class="sigplot"></div>
</template>

<script>
import sigplot from 'sigplot';

export default {
  name: 'SigPlot',
  props: {
    plotOptions: {
      type: Object,
      default: () => {}
    },
  },
  // watch() {
  //   options: {
  //     handler (newValue) {
  //       this.chart.update(copyObject(newValue, this.deepCopyOnUpdate), ...this.updateArgs)
  //     },
  //     deep: true
  //   }
  // },
  mounted() {
    this.plot = new sigplot.Plot(this.$el, this.plotOptions)
  },

  beforeDestroy () {
    if (this.plot) {
      /* @TODO: do something... */
    }
  }
}
</script>

<style>
div.sigplot {
  height: 300px;
  width: 300px;
}
</style>
