# contains(selector)

Asserte que chaque `Wrapper` de `WrapperArray` contient un élément basé sur un sélecteur.
Utilisez n'importe quels [sélecteurs](../selectors.md).

- **Paramètres :**
  - `{string|Component} selector : sélecteur`

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { shallow } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'
import Bar from './Bar.vue'

const wrapper = shallow(Foo)
const divArray = wrapper.findAll('div')
expect(divArray.contains('p')).toBe(true)
expect(divArray.contains(Bar)).toBe(true)
```
