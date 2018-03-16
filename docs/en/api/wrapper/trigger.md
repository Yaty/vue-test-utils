# trigger(eventName)

Déclenche un évènement sur le nœud du DOM du `Wrapper`.

`Trigger` prend un objet optionel `options`. Les propriétés dans `options` sont ajoutées à l'évènement.

Vous pouvez activer `preventDefault` sur l'évènement en passant `preventDefault: true` dans `options`.

- **Paramètres :**
  - `{string} eventName : nom de l'évènement`
  - `{Object} options`
    - `{boolean} preventDefault`

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import sinon from 'sinon'
import Foo from './Foo'

const clickHandler = sinon.stub()
const wrapper = mount(Foo, {
  propsData: { clickHandler }
})

wrapper.trigger('click')

wrapper.trigger('click', {
  button: 0
})

wrapper.trigger('click', {
  preventDefault: true
})

expect(clickHandler.called).toBe(true)
```
