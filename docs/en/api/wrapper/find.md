# find(selector)

Retourne un [`Wrapper`](README.md) du premier nœud du DOM ou le composant Vue correspondant au sélecteur.

Utilise n'importe quels [sélecteurs valides](../selectors.md).

- **Paramètres **
  - `{string|Component} selector : un sélecteur`

- **Retourne :** `{Wrapper}`

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'
import Bar from './Bar.vue'

const wrapper = mount(Foo)
const div = wrapper.find('div')
expect(div.is('div')).toBe(true)
const bar = wrapper.find(Bar)
expect(bar.is(Bar)).toBe(true)
```

- **Voir aussi :** [Wrapper](README.md)
