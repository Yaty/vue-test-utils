# `setMethods(methods)`

Fixe les méthodes de l'instance de Vue `vm` du `Wrapper` et force la mise à jour sur chaque `Wrapper` de `WrapperArray`.

**Note : chaque `Wrapper` doit contenir une instance de Vue.**

- **Paramètre :**
  - `{Object} methods`

- **Exemple :**

```js
import { mount } from '@vue/test-utils'
import sinon from 'sinon'
import Foo from './Foo.vue'
import Bar from './Bar.vue'

const wrapper = mount(Foo)
const barArray = wrapper.findAll(Bar)
const clickMethodStub = sinon.stub()

barArray.setMethods({ clickMethod: clickMethodStub })
barArray.at(0).trigger('click')
expect(clickMethodStub.called).toBe(true)
```
