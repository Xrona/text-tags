<template>
  <div class="wrapper">
    <div class="wrapper__options">
      <v-text-field
        label="Width"
        hide-details="auto"
        v-model="widthContent"
      ></v-text-field>
      <v-text-field
        label="Height"
        hide-details="auto"
        v-model="heightContent"
      ></v-text-field>
      <v-btn depressed color="primary" @click="setAlign('left')"> Left </v-btn>
      <v-btn depressed color="primary" @click="setAlign('justify')">
        Justify
      </v-btn>
    </div>
    <div
      class="wrapper__object"
      :style="`width: ${width}px; height: ${height}px;`"
    >
      <slot />
    </div>
  </div>
</template>

<script>
export default {
  name: 'WrapperItem',

  props: {
    width: {
      type: String,
      required: true,
    },
    height: {
      type: String,
      required: true,
    },
    align: {
      type: String,
      default: 'left',
    },
  },

  computed: {
    widthContent: {
      get() {
        return this.width
      },
      set(value) {
        this.$emit('setWidth', value)
      },
    },
    heightContent: {
      get() {
        return this.height
      },
      set(value) {
        this.$emit('setHeight', value)
      },
    },
    alignContent: {
      get() {
        return this.align
      },
      set(value) {
        this.$emit('setAlign', value)
      },
    },
  },

  methods: {
    setAlign(value) {
      this.alignContent = value
    },
  },
}
</script>
