# `emittedByOrder()`

Retourne un tableau contenant des évènements émis personnalisés par l'instance de Vue `vm` de `Wrapper`.

- **Retourne :** `Array<{ name: string, args: Array<any> }>`

- **Exemple :**

```js
import { mount } from '@vue/test-utils'

const wrapper = mount(Component)

wrapper.vm.$emit('foo')
wrapper.vm.$emit('bar', 123)

/*
wrapper.emittedByOrder() retourne le tableau suivant :
[
  { name: 'foo', args: [] },
  { name: 'bar', args: [123] }
]
*/

// asserte l'ordre des émissions
expect(wrapper.emittedByOrder().map(e => e.name)).toEqual(['foo', 'bar'])
```
