# `at(index)`

Retourne le `Wrapper` à l'index passé en paramètre. L'indexation commence à 0.

- **Paramètre :**
  - `{number} index`

- **Retourne :** `{Wrapper}`

- **Exemple :**

```js
import { shallow } from '@vue/test-utils'
import Foo from './Foo.vue'

const wrapper = shallow(Foo)
const divArray = wrapper.findAll('div')
const secondDiv = divArray.at(1)
expect(secondDiv.is('p')).toBe(true)
```
