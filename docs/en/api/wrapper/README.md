# `Wrapper`

`vue-test-utils` est une API basée sur un `wrapper`.

Un `Wrapper` est un objet qui contient un composant monté, un nœud virtuel et des méthodes pour les tester.

- **Propriétés :**

`vm` `Component`: c'est une instance de Vue. Vous pouvez accéder à toutes les [méthodes et propriétés de l'instance](https://vuejs.org/v2/api/#Instance-Properties) avec `wrapper.vm`. Cela existe uniquement sur les `wrappers` de composants Vue.
`element` `HTMLElement`: le nœud principal du DOM du `wrapper`.
`options` `Object`: objet contenant les options de `vue-test-utils` passées à `mount` ou `shallow`.
`options.attachedToDom` `Boolean`: `true` si `attachToDom` est passé à `mount` ou `shallow`.

- **Méthodes :**

Il y a une liste détaillé des méthodes dans la section `wrapper` de la documentation.