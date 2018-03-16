# `contains(selector)`

Asserte que chaque `Wrapper` de `WrapperArray` contient un élément basé sur un sélecteur.

- **Paramètres :**
  - `{string|Component} selector : sélecteur`

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { shallow } from '@vue/test-utils'
import Foo from './Foo.vue'
import Bar from './Bar.vue'

const wrapper = shallow(Foo)
const divArray = wrapper.findAll('div')
expect(divArray.contains('p')).toBe(true)
expect(divArray.contains(Bar)).toBe(true)
```
