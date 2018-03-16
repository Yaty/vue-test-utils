# hasClass(className)

Asserte que chaque `Wrapper` de `WrapperArray` a un nœud du DOM qui a une classe contenant `className`.

- **Paramètre :**
  - `{string} className : nom d'une classe`

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
const divArray = wrapper.findAll('div')
expect(divArray.hasClass('bar')).toBe(true)
```
