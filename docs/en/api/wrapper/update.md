# update()

Force le composant Vue principal à se mettre à jour.

Si appellée sur un `Wrapper` contenant une instance de Vue `vm`, il la mettra à jour.

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
expect(wrapper.vm.bar).toBe('bar')
wrapper.vm.bar = 'nouvelle valeur'
wrapper.update()
expect(wrapper.vm.bar).toBe('nouvelle valeur')
```
