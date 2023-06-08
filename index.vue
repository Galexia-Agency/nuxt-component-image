<template>
  <picture>
    <source type="image/avif" :srcset="avif" :width="width" :height="height">
    <img
      :src="webp"
      :decoding="decoding"
      :loading="loading"
      :alt="alt"
      :width="width"
      :height="height"
      :fetchpriority="fetchpriority"
    >
  </picture>
</template>

<script>
export default {
  name: 'Galexia_NuxtComponent_Image',
  props: {
    webp: {
      type: Object,
      required: true
    },
    avif: {
      type: Object,
      required: true
    },
    width: {
      type: [Number, String],
      default: 'auto'
    },
    height: {
      type: [Number, String],
      default: 'auto'
    },
    loading: {
      type: String,
      default: 'lazy'
    },
    decoding: {
      type: String,
      default: 'async'
    },
    fetchpriority: {
      type: String,
      default: 'auto'
    },
    alt: {
      type: String,
      default: ''
    }
  }
}
</script>
