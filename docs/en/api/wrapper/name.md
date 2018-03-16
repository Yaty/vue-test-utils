# `name()`

Retourne le nom du composant si le `Wrapper` contient une instance de Vue. Il retourne le nom de la balise du nœud du DOM du `Wrapper` si il ne contient pas une instance de Vue. 

- **Retourne :** `{string}`

- **Exemple :**

```js
import { mount } from '@vue/test-utils'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
expect(wrapper.name()).toBe('Foo')
const p = wrapper.find('p')
expect(p.name()).toBe('p')
```
