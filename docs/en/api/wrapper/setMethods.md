# `setMethods(methods)`

Fixe les méthodes de l'instance de Vue `vm` du `Wrapper` `vm` et force la mise à jour.

**Note : le `Wrapper` doit contenir une instance de Vue.**

- **Paramètres:**
  - `{Object} methods`

- **Exemple :**

```js
import { mount } from '@vue/test-utils'
import sinon from 'sinon'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
const clickMethodStub = sinon.stub()

wrapper.setMethods({ clickMethod: clickMethodStub })
wrapper.find('button').trigger('click')
expect(clickMethodStub.called).toBe(true)
```
