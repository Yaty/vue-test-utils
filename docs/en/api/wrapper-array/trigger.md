# `trigger(eventName)`

Déclenche un évènement sur chaque nœud du DOM des `Wrapper` de `WrapperArray`.

**Note : chaque `Wrapper` doit contenir une instance de Vue.**

- **Paramètre :**
  - `{string} eventName ; nom de l'évènement`

- **Exemple :**

```js
import { mount } from '@vue/test-utils'
import sinon from 'sinon'
import Foo from './Foo.vue'

const clickHandler = sinon.stub()
const wrapper = mount(Foo, {
  propsData: { clickHandler }
})

const divArray = wrapper.findAll('div')
divArray.trigger('click')
expect(clickHandler.called).toBe(true)
```
