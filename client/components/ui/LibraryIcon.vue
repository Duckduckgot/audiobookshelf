<template>
  <div :class="`h-${size} w-${size} min-w-${size} text-${fontSize}`" class="flex items-center justify-center">
    <span class="abs-icons" :class="`icon-${iconToUse}`"></span>
  </div>
</template>

<script>
export default {
  props: {
    icon: {
      type: String,
      default: 'kepseebook'
    },
    fontSize: {
      type: String,
      default: 'lg'
    },
    size: {
      type: Number,
      default: 5
    }
  },
  data() {
    return {}
  },
  computed: {
    iconToUse() {
      return this.icons.includes(this.icon) ? this.icon : 'kepseebook'
    },
    icons() {
      return this.$store.state.globals.libraryIcons
    }
  },
  methods: {},
  mounted() {}
}
</script>
