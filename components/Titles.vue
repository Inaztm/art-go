<template lang="pug">
  header.titles
    section
      div(v-if="smallTitle").titles__small {{ smallTitle }}
      h2(v-if="bigTitle").titles__big {{ bigTitle }}
    section
      slot
</template>

<script>
export default {
  name: 'titles',
  props: {
    bigTitle: {
      type: String,
      default: null
    },
    smallTitle: {
      type: String,
      default: null
    }
  }
}
</script>

