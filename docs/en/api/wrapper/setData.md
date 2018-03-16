# `setData(data)`

Fixe les données de l'instance de Vue `vm` du `Wrapper` `vm` et force la mise à jour.

**Note : le `Wrapper` doit contenir une instance de Vue.**

- **Paramètres :**
  - `{Object} data : données`

- **Exemple :**

```js
import { mount } from '@vue/test-utils'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
wrapper.setData({ foo: 'bar' })
expect(wrapper.vm.foo).toBe('bar')
```
