# `update()`

Force le composant Vue principal de chaque `Wrapper` de `WrapperArray` à se mettre à jour.

Si appellée sur `WrapperArray`, il mettra à jour le composant de chaque `Wrapper`.

- **Exemple :**

```js
import { mount } from '@vue/test-utils'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
const divArray = wrapper.findAll('div')
expect(divArray.at(0).vm.bar).toBe('bar')
divArray.at(0).vm.bar = 'nouvelle valeur'
divArray.update()
expect(divArray.at(0).vm.bar).toBe('nouvelle valeur')
```
