# hasProp(prop, value)

Asserte que l'instance de Vue `vm` du `Wrapper` contient une `prop` de valeur `value`.

Retourne `true` si l'instance de Vue `vm` du `Wrapper` contient une `prop` de valeur `value`.


**Note : le Wrapper doit posséder une instance de Vue.**

- **Paramètres :**
  - `{string} prop`
  - `{any} value`

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
expect(wrapper.hasProp('bar', 10)).toBe(true)
```
