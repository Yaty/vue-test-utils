# createLocalVue()

- **Retourne :**
  - `{Component}`

- **Utilisation :**

`createLocalVue` retourne une classe de Vue pour ajouter des composants, des mixins et installer des plugins sans polluer la classe globale Vue.

Utilisez la avec `options.localVue`

```js
import { createLocalVue, shallow } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'

const localVue = createLocalVue()
const wrapper = shallow(Foo, {
  localVue,
  mocks: { foo: true }
})
expect(wrapper.vm.foo).toBe(true)

const freshWrapper = shallow(Foo)
expect(freshWrapper.vm.foo).toBe(false)
```

- **Voir aussi :** [Astuces](../guides/common-tips.md#applying-global-plugins-and-mixins)
