# `isEmpty()`

Asserte que le `Wrapper` ne contient pas de nœuds enfants.

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { mount } from '@vue/test-utils'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
expect(wrapper.isEmpty()).toBe(true)
```
