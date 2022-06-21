<template>
  <span class="tag-list__item">
    <v-icon v-if="idx > 0">mdi-circle-small</v-icon>
    <span class="tag-list__name">{{ name }}</span>
  </span>
</template>

<script>
export default {
  name: 'TagItem',

  props: {
    idx: {
      type: Number,
      required: true,
    },
    name: {
      type: String,
      required: true,
    },
  },
}
</script>
