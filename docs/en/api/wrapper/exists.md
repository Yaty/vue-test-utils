# `exists()`

Asserte que `Wrapper` ou `WrapperArray` existent.

Retourne `false` si appelé sur un `Wrapper` ou `WrapperArray` vide.

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { mount } from '@vue/test-utils'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
expect(wrapper.exists()).toBe(true)
expect(wrapper.find('does-not-exist').exists()).toBe(false)
expect(wrapper.findAll('div').exists()).toBe(true)
expect(wrapper.findAll('does-not-exist').exists()).toBe(false)
```
