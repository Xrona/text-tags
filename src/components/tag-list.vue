<template>
  <p
    id="tagList"
    :style="`text-align: ${align}; --lines: ${lines}`"
    class="tag-list"
    ref="tagList"
  >
    <span class="tag-list__icon">
      <v-icon>{{ iconName }}</v-icon>
    </span>
    <template v-for="(item, idx) in tagItems">
      <tag-item :key="`${item} ${idx}`" :name="item" :idx="idx" />
    </template>
  </p>
</template>

<script>
import tagItem from './tag-item.vue'
export default {
  components: { tagItem },

  name: 'TagList',

  props: {
    items: {
      type: Array,
      default: Array,
    },
    align: {
      type: String,
      default: 'left',
    },
    heightWrapper: {
      type: String,
      default: '',
    },
  },

  data() {
    return {
      tagItems: [],
      iconName: '',
      lines: 0,
    }
  },

  watch: {
    heightWrapper() {
      this.countLines()
    },
  },

  mounted() {
    const items = [...this.items]
    this.iconName = items.shift()
    this.tagItems = items
    this.countLines()

    window.addEventListener('resize', this.countLines)
  },

  beforeDestroy() {
    window.removeEventListener('resize', this.countLines)
  },

  methods: {
    countLines() {
      const wrapper = this.$refs.tagList.parentNode
      const height = wrapper.getBoundingClientRect()?.height ?? 0
      console.log(height, Math.floor(height / 22))

      this.lines = Math.floor(height / 24)
    },
  },
}
</script>
