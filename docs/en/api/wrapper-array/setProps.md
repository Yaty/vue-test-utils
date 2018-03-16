# setProps(props)

Fixe les `props` de l'instance de Vue `vm` du `Wrapper` et force la mise à jour sur chaque `Wrapper` de `WrapperArray`.

**Note : chaque `Wrapper` doit contenir une instance de Vue.**

- **Paramètre :**
  - `{Object} props`

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'
import Bar from './Bar.vue'

const wrapper = mount(Foo)
const barArray = wrapper.findAll(Bar)
barArray.setProps({ foo: 'bar' })
expect(barArray.at(0).vm.foo).toBe('bar')
```
