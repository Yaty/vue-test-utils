# `is(selector)`

Asserte que le DOM du `Wrapper` ou que l'instance de Vue `vm` correspond au [sélecteur](../selectors.md).

- **Paramètres :**
  - `{string|Component} selector : un sélecteur`

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { mount } from '@vue/test-utils'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
expect(wrapper.is('div')).toBe(true)
```
