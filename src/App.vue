<template>
  <v-app>
    <v-main>
      <v-container>
        <wrapper-item
          :width="width1"
          :height="height1"
          :align="align1"
          @setWidth="widthHandler1"
          @setHeight="heightHandler1"
          @setAlign="alignHandler1"
        >
          <tag-list
            :items="$options.items"
            :align="align1"
            :heightWrapper="height1"
          />
        </wrapper-item>
        <wrapper-item
          :width="width2"
          :height="height2"
          :align="align2"
          @setWidth="widthHandler2"
          @setHeight="heightHandler2"
          @setAlign="alignHandler2"
        >
          <tag-list
            :items="$options.items"
            :align="align2"
            :heightWrapper="height2"
          />
        </wrapper-item>
        <wrapper-item
          :width="width3"
          :height="height3"
          :align="align3"
          @setWidth="widthHandler3"
          @setHeight="heightHandler3"
          @setAlign="alignHandler3"
        >
          <tag-list
            :items="$options.items"
            :align="align3"
            :heightWrapper="height3"
          />
        </wrapper-item>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import TagList from '@/components/tag-list.vue'
import WrapperItem from '@/components/wrapper-item.vue'
export default {
  name: 'App',

  components: { TagList, WrapperItem },

  data() {
    return {
      width1: '300',
      height1: '200',
      align1: 'left',
      width2: '600',
      height2: '400',
      align2: 'left',
      width3: '800',
      height3: '300',
      align3: 'left',
    }
  },

  methods: {
    widthHandler1(value) {
      this.width1 = value
    },
    widthHandler2(value) {
      this.width2 = value
    },
    widthHandler3(value) {
      this.width3 = value
    },
    heightHandler1(value) {
      this.height1 = value
    },
    heightHandler2(value) {
      this.height2 = value
    },
    heightHandler3(value) {
      this.height3 = value
    },
    alignHandler1(value) {
      this.align1 = value
    },
    alignHandler2(value) {
      this.align2 = value
    },
    alignHandler3(value) {
      this.align3 = value
    },
  },

  items: [
    'mdi-star-outline',
    'Lorem Ipsum',
    'is simply dummy',
    'text of',
    'the printing and',
    'typesetting',
    'industry lorem Ipsum has been',
    'the industrys standard dummy',
    'text',
    'ever',
    'since the 1500s, when an unknown',
    'printer took',
    'a galley of type and',
    'scrambled it',
    'to make a type specimen book.',
    'It has survived',
    'not only five centuries',
    'but also',
    'the leap into electronic',
    'typesetting',
    'remaining essentially',
    'unchanged',
    'It was popularised',
    'in the 1960s with the release of Letraset sheets containing',
    'Lorem Ipsum passages',
    'and more recently with',
    'desktop publishing software like Aldus',
    'PageMaker including versions of Lorem Ipsum.',
    'mdi-star-outline',
    'Lorem Ipsum',
    'is simply dummy',
    'text of',
    'the printing and',
    'typesetting',
    'industry lorem Ipsum has been',
    'the industrys standard dummy',
    'text',
    'ever',
    'since the 1500s, when an unknown',
    'printer took',
    'a galley of type and',
    'scrambled it',
    'to make a type specimen book.',
    'It has survived',
    'not only five centuries',
    'but also',
    'the leap into electronic',
    'typesetting',
    'remaining essentially',
    'unchanged',
    'It was popularised',
    'in the 1960s with the release of Letraset sheets containing',
    'Lorem Ipsum passages',
    'and more recently with',
    'desktop publishing software like Aldus',
    'PageMaker including versions of Lorem Ipsum.',
    'mdi-star-outline',
    'Lorem Ipsum',
    'is simply dummy',
    'text of',
    'the printing and',
    'typesetting',
    'industry lorem Ipsum has been',
    'the industrys standard dummy',
    'text',
    'ever',
    'since the 1500s, when an unknown',
    'printer took',
    'a galley of type and',
    'scrambled it',
    'to make a type specimen book.',
    'It has survived',
    'not only five centuries',
    'but also',
    'the leap into electronic',
    'typesetting',
    'remaining',
    'essentially unchanged',
    'It was popularised',
    'in the 1960s with the release of Letraset sheets containing',
    'Lorem Ipsum passages',
    'and more recently with',
    'desktop publishing software like Aldus',
    'PageMaker including versions of Lorem Ipsum.',
    'mdi-star-outline',
    'Lorem Ipsum',
    'is simply dummy',
    'text of',
    'the printing and',
    'typesetting',
    'industry lorem Ipsum has been',
    'the industrys standard dummy',
    'text',
    'ever',
    'since the 1500s, when an unknown',
    'printer took',
    'a galley of type and',
    'scrambled it',
    'to make a type specimen book.',
    'It has survived',
    'not only five centuries',
    'but also',
    'the leap into electronic',
    'typesetting',
    'remaining essentially',
    'unchanged',
    'It was popularised',
    'in the 1960s with the release of Letraset sheets containing',
    'Lorem Ipsum passages',
    'and more recently with',
    'desktop publishing software like Aldus',
    'PageMaker including versions of Lorem Ipsum.',
    'mdi-star-outline',
    'Lorem Ipsum',
    'is simply dummy',
    'text of',
    'the printing and',
    'typesetting',
    'industry lorem Ipsum has been',
    'the industrys standard dummy',
    'text',
    'ever',
    'since the 1500s, when an unknown',
    'printer took',
    'a galley of type and',
    'scrambled it',
    'to make a type specimen book.',
    'It has survived',
    'not only five centuries',
    'but also',
    'the leap into electronic',
    'typesetting',
    'remaining essentially',
    'unchanged',
    'It was popularised',
    'in the 1960s with the release of Letraset sheets containing',
    'Lorem Ipsum passages',
    'and more recently with',
    'desktop publishing software like Aldus',
    'PageMaker including versions of Lorem Ipsum.',
  ],
}
</script>

<style lang="scss">
@import './app.scss';
</style>
