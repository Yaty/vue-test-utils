# `trigger(eventName)`

Déclenche un évènement sur le nœud du DOM du `Wrapper`.

`Trigger` prend un objet optionel `options`. Les propriétés dans `options` sont ajoutées à l'évènement.

- **Paramètres :**
  - `{string} eventName : nom de l'évènement`
  - `{Object} options`

- **Exemple :**

```js
import { mount } from '@vue/test-utils'
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

expect(clickHandler.called).toBe(true)
```
- **Setting the event target:**

Under the hood, `trigger` creates an `Event` object and dispatches the event on the Wrapper element.

It's not possible to edit the `target` value of an `Event` object, so you can't set `target` in the options object.

To add an attribute to the `target`, you need to set the value of the Wrapper element before calling `trigger`. You can do this with the `element` property.

```js
const input = wrapper.find('input')
input.element.value = 100
input.trigger('click')
```
