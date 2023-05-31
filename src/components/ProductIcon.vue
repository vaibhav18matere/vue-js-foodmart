<template>
     <Icon v-bind="bindings" />
</template>

<script>

export default {
  props: ['product'],
  computed: {
    bindings () {
      return {
        ...this.$attrs,
        name: this.product.icon,
        class: `icofont-10x  icofont-${[this.product.icon]}`
      }
    }
  }
}
</script>
