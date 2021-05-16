# vue-remote-components-loader
Dynamically load a Vue Component from a URL
#### Only Support CSR Component
## Install

```
yarn add vue-remote-components-loader
```

## Start

```javascript
// create
this.$dynamicComponent.create(Component)
// pkg
// umd
"build:module": "vue-cli-service build --target lib src/module.js --name web-invite"
```

```javascript
// 导入插件
import Vue from 'vue'
import loader from 'vue-remote-components-loader'
Vue.use(loader, { router, store })
// * or manual
// import { dynamicComponentState, dynamicComponent } from 'vue-remote-components-loader'
// store.registerModule('dynamicComponentState', dynamicComponentState)
// Vue.prototype.$dynamicComponent = dynamicComponent(store)
const app = new Vue({...})

// use a remote component
app.$moduleLoader({
  module1: '//xxx/module1.js'
})
// use local component
import component from './component'
app.$moduleLoader(component)
```
