# hasStyle(style, value)

Asserte que le DOM du `Wrapper` contient un style avec une certaine valeur.

Retourne `true` si le nœud du DOM du `Wrapper` contient un `style` correspondant à `string`.

**Note : cela va uniquement détecter les styles `inlines` quand ils fonctionnent avec `jsdom`.**

- **Paramètres :**
  - `{string} style`
  - `{string} value`

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
expect(wrapper.hasStyle('color', 'red')).toBe(true)
```
