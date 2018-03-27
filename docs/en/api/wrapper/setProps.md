# `setProps(props)`

- **Paramètres :**
  - `{Object} props`

- **Exemple :**

Assigne les `props` de l'instance de Vue `vm` du `Wrapper` `vm` et force la mise à jour.

**Note : le `Wrapper` doit contenir une instance de Vue.**

```js
import { mount } from '@vue/test-utils'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
wrapper.setProps({ foo: 'bar' })
expect(wrapper.vm.foo).toBe('bar')
```

Vous pouvez aussi passer un objet `propsData`, qui initialisera l'instance de Vue avec des données.

``` js
// Foo.vue
export default {
  props: {
    foo: {
      type: String,
      required: true
    }
  }
}
```

``` js
import { mount } from '@vue/test-utils'
import Foo from './Foo.vue'

const wrapper = mount(Foo, {
  propsData: {
    foo: 'bar'
  }
})

expect(wrapper.vm.foo).toBe('bar')
```
