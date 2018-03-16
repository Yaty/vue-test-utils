# emitted()

Retourne un objet contenant des évènements émis par l'instance de Vue `vm` du `Wrapper`.

- **Retourne :** `{ [name: string]: Array<Array<any>> }`

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'

const wrapper = mount(Component)

wrapper.vm.$emit('foo')
wrapper.vm.$emit('foo', 123)

/*
wrapper.emitted() retourne l'objet suivant :
{
  foo: [[], [123]]
}
*/

// asserte que l'évènement est émis
expect(wrapper.emitted().foo).toBeTruthy()

// asserte que l'évènement est compté
expect(wrapper.emitted().foo.length).toBe(2)

// asserte le contenu de l'évènement
expect(wrapper.emitted().foo[1]).toEqual([123])
```
