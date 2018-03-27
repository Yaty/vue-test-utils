# `update()`

Force le composant racine de Vue à se mettre à jour.

Si appelée sur un `Wrapper` contenant une instance de Vue `vm`, cela forcera le `Wrapper` à la re-rendre.

- **Exemple :**

```js
import { mount } from '@vue/test-utils'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
expect(wrapper.vm.bar).toBe('bar')
wrapper.vm.bar = 'nouvelle valeur'
wrapper.update()
expect(wrapper.vm.bar).toBe('nouvelle valeur')
```
