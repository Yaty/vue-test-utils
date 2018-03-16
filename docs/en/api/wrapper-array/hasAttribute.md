# hasAttribute(attribute, value)

Asserte que chaque `Wrapper` de `WrapperArray` a un nœud du DOM qui à un attribut (`attribute`) ayant une certaine valeur (`value`).

- **Paramètres :**
  - `{string} attribute : l'attribut`
  - `{string} value : la valeur`

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
const divArray = wrapper.findAll('div')
expect(divArray.hasAttribute('id', 'foo')).toBe(true)
```
