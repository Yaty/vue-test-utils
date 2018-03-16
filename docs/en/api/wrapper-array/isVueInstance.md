# isVueInstance()

Asserte que chaque `Wrapper` de `WrapperArray` possède une instance de Vue.

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'
import Bar from './Bar.vue'

const wrapper = mount(Foo)
const barArray = wrapper.findAll(Bar)
expect(barArray.isVueInstance()).toBe(true)
```
