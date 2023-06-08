# Galexia Nuxt Component Image

## Install

### Pre-Requisites

We assume you have a Nuxt project.
You'll need to install [Nuxt Optimized Images](https://www.npmjs.com/package/@aceforth/nuxt-optimized-images) first.

```bash
yarn add --dev @aceforth/nuxt-optimized-images responsive-loader sharp
```

```js
// nuxt.config.js
...
modules: [
  '@aceforth/nuxt-optimized-images'
],
optimizedImages: {
  optimizeImages: true,
  optimizeImagesInDev: true
},
...
```

### You can now install this package

```bash
yarn add https://github.com/Galexia-Agency/nuxt-component-image
```

```js
// plugins/galexia/nuxt-components/image.js
import Vue from 'vue'
import Galexia_NuxtComponent_Image from 'nuxt-component-image/index.vue'

Vue.component('GalexiaImage', Galexia_NuxtComponent_Image)
```

```js
// nuxt.config.js
...
plugins: [
  '~plugins/galexia/components/image.js'
],
...
```

### And use it like so

```js
// pages/index.js
<GalexiaImage
  class="page-header__image"
  :avif="require('~/assets/img/joe-bailey.jpg?format=avif&resize&size=150')"
  :webp="require('~/assets/img/joe-bailey.jpg?format=webp&resize&size=150')"
  width="150"
  loading="eager"
  fetchpriority="high"
  alt="Joe Bailey Portrait"
/>
```
