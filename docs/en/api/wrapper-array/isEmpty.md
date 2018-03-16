# isEmpty()

Asserte que chaque `Wrapper` de `WrapperArray` ne contient pas de nœuds enfants.

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
const divArray = wrapper.findAll('div')
expect(divArray.isEmpty()).toBe(true)
```
