# setProps(props)

- **Paramètres :**
  - `{Object} props`

- **Exemple :**

Fixe les `props` de l'instance de Vue `vm` du `Wrapper` `vm` et force la mise à jour.
Sets `Wrapper` `vm` props and forces update.
**Note : le `Wrapper` doit contenir une instance de Vue.**

**Note the Wrapper must contain a Vue instance.**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
wrapper.setProps({ foo: 'bar' })
expect(wrapper.props().foo).toBe('bar')
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
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'

const wrapper = mount(Foo, {
  propsData: {
    foo: 'bar'
  }
})

expect(wrapper.vm.foo).to.equal('bar')
```
