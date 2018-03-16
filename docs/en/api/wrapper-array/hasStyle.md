# hasStyle(style, value)

Asserte que chaque `Wrapper` de `WrapperArray` a un nœud DOM ayant un certain style avec une certaine valeur (`value`).

Retourne `true` si le nœud du DOM du `Wrapper` contient un `style` correspondant à `value`.

**Note : cela va uniquement détecter les styles `inlines` en cours d'exécution dans `jsdom`.**
- **Paramètres :**
  - `{string} style`
  - `{string} value : valeur`

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
const divArray = wrapper.findAll('div')
expect(divArray.hasStyle('color', 'red')).toBe(true)
```
