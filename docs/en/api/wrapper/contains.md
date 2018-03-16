# contains(selector)

Asserte que `Wrapper` contient un élément ou un composant correspondant au [sélecteur](../selectors.md).

- **Paramètres :**
  - `{string|Component} selector : un sélecteur`

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'
import Bar from './Bar.vue'

const wrapper = mount(Foo)
expect(wrapper.contains('p')).toBe(true)
expect(wrapper.contains(Bar)).toBe(true)
```

- **Voir aussi :** [sélecteurs](../selectors.md)
