# hasProp(prop, value)

Asserte que chaque instance de Vue `vm` de `Wrapper` dans `WrapperArray` a une `prop` correspondant à `value`.

**Note : le `Wrapper` doit contenir une instance de Vue.**

- **Paramètres :**
  - `{string} prop`
  - `{any} value : la valeur`

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'
import Bar from './Bar.vue'

const wrapper = mount(Foo)
const barArray = wrapper.findAll(Bar)
expect(barArray.hasProp('bar', 10)).toBe(true)
```
