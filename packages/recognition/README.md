<div style="text-align: center;" align="center">

# use-recognition

A composition api for SpeechRecognition, supports vue2.0 and vue3.0

[![NPM version][npm-image]][npm-url]
[![Codacy Badge][codacy-image]][codacy-url]
[![Test coverage][codecov-image]][codecov-url]
[![npm download][download-image]][download-url]
[![gzip][gzip-image]][gzip-url]
[![License][license-image]][license-url]

[![Sonar][sonar-image]][sonar-url]

</div>

<div style="text-align: center; margin-bottom: 20px;" align="center">

</div>

## Installing

```bash
# use pnpm
$ pnpm install use-recognition

# use npm
$ npm install use-recognition --save

# use yarn
$ yarn add use-recognition
```

## Usage

### Use in Vue `>=3.0`

```vue
<script setup>
import { getCurrentInstance, onMounted } from 'vue'
import useRecognition from 'use-recognition'

const recognition = useRecognition({ lang: 'zh_CN' })

onMounted(() => {
  recognition.start()
})

useExpose({ recognition })
</script>
```

### Use in Vue `2.7`

```vue
<script>
import useRecognition from 'use-recognition'

export default {
  setup() {
    const recognition = useRecognition({ lang: 'zh_CN' })
    recognition.start()

    return { recognition }
  }
}
</script>
```

### Use in Vue `<=2.6`

> Add `@vue/composition-api` to the `project.json` dependencies and run install.

```json
{
  "dependencies": {
    "@vue/composition-api": "latest"
  }
}
```

```js
// main.js
import Vue from 'vue'
import VueCompositionApi from '@vue/composition-api'

Vue.use(VueCompositionApi)

new Vue({}).$mount('#app')
```

```vue
<script>
import useRecognition from 'use-recognition'

export default {
  setup() {
    const recognition = useRecognition({ lang: 'zh_CN' })
    recognition.start()

    return { recognition }
  }
}
</script>
```

### Using unpkg CDN

```html
<script src="https://unpkg.com/vue-demi@latest/lib/index.iife.js"></script>
<script src="https://unpkg.com/use-recognition@1.0.0/dist/index.global.prod.js"></script>
```

## Support & Issues

Please open an issue [here](https://github.com/saqqdy/uni-use/issues).

## License

[MIT](LICENSE)

[npm-image]: https://img.shields.io/npm/v/use-recognition.svg?style=flat-square
[npm-url]: https://npmjs.org/package/use-recognition
[codacy-image]: https://app.codacy.com/project/badge/Grade/f70d4880e4ad4f40aa970eb9ee9d0696
[codacy-url]: https://www.codacy.com/gh/saqqdy/use-recognition/dashboard?utm_source=github.com&utm_medium=referral&utm_content=saqqdy/use-recognition&utm_campaign=Badge_Grade
[codecov-image]: https://img.shields.io/codecov/c/github/saqqdy/use-recognition.svg?style=flat-square
[codecov-url]: https://codecov.io/github/saqqdy/use-recognition?branch=master
[download-image]: https://img.shields.io/npm/dm/use-recognition.svg?style=flat-square
[download-url]: https://npmjs.org/package/use-recognition
[gzip-image]: http://img.badgesize.io/https://unpkg.com/use-recognition/dist/index.global.prod.js?compression=gzip&label=gzip%20size:%20JS
[gzip-url]: http://img.badgesize.io/https://unpkg.com/use-recognition/dist/index.global.prod.js?compression=gzip&label=gzip%20size:%20JS
[license-image]: https://img.shields.io/badge/License-MIT-blue.svg
[license-url]: LICENSE
[sonar-image]: https://sonarcloud.io/api/project_badges/quality_gate?project=saqqdy_uni-use
[sonar-url]: https://sonarcloud.io/dashboard?id=saqqdy_uni-use
