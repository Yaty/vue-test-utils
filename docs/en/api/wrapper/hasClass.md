# hasClass(className)

Asserte que le DOM du `Wrapper` contient une classe nommé `className`.

Retourne `true` si le nœud du DOM du `Wrapper` contient la classe.

- **Paramètres :**
  - `{string} className`

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
expect(wrapper.hasClass('bar')).toBe(true)
```
