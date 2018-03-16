# exists()

Asserte que `Wrapper` ou `WrapperArray` existent.

Retourne `false` si appellé sur un `Wrapper` ou `WrapperArray` vide.

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
expect(wrapper.exists()).toBe(true)
expect(wrapper.find('existe-pas').exists()).toBe(false)
expect(wrapper.findAll('div').exists()).toBe(true)
expect(wrapper.findAll('existe-pas').exists()).toBe(false)
```
