# `is(selector)`

Asserte que chaque `Wrapper` de `WrapperArray` a un nœud du DOM ou une instance de Vue `vm` correspondant à un [sélecteur](../selectors.md).

- **Paramètre :**
  - `{string|Component} selector : un sélecteur`

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { mount } from '@vue/test-utils'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
const divArray = wrapper.find('div')
expect(divArray.is('div')).toBe(true)
```
