<template lang="pug">
  .hero(:style="`background-image: url(${lowres})`")
    img.hero-background(:src="image")
    slot
    .hero-title(:class="{'hero-title-jp': $store.state.i18n.locale === 'jp'}") {{ copy }}
</template>

<script>
export default {
  props: {
    lowres: {
      type: String,
      required: true,
    },
    image: {
      type: String,
      required: true,
    },
    copy: {
      type: String,
      required: true,
    },
  }
}
</script>
