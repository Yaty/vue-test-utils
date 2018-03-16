# hasAttribute(attribute, value)

Asserte que le DOM du `Wrapper` a l'attribut avec la valeur correspondate.

Retourne `true` si le nœud du DOM du `Wrapper` contient un attribut avec la bonne valeur.

- **Paramètres :**
  - `{string} attribute`
  - `{string} value`

- **Retourne :** `{boolean}`

- **Exemple :**

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
expect(wrapper.hasAttribute('id', 'foo')).toBe(true)
```

- **Alternative :**

Vous pouvez récuperer l'attribut depuis `Wrapper.element` pour avoir une assertion basée sur une valeur.

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'

const wrapper = mount(Foo)
expect(wrapper.element.getAttribute('id')).toBe('foo')
```

Cela produit une erreur d'assertion plus informative.