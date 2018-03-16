# `findAll(selector)`

Retourne un [`WrapperArray`](../wrapper-array/README.md) de [Wrappers](README.md).

Utilise n'importe quels [sélecteurs valides](../selectors.md).

- **Paramètres :**
  - `{string|Component} selector : un sélecteur`

- **Retourne :** `{WrapperArray}`

- **Exemple :**

```js
import { mount } from '@vue/test-utils'
import Foo from './Foo.vue'
import Bar from './Bar.vue'

const wrapper = mount(Foo)
const div = wrapper.findAll('div').at(0)
expect(div.is('div')).toBe(true)
const bar = wrapper.findAll(Bar).at(0)
expect(bar.is(Bar)).toBe(true)
```

- **Voir aussi :** [Wrapper](README.md)
