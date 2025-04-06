# Ejemplo: `$bindable()` + `bind:` con múltiples componentes

Este ejemplo muestra cómo se puede sincronizar una variable (`name`) entre un componente padre y dos componentes hijos usando las nuevas *runes* de Svelte 5.

## 🧠 Concepto clave

Al usar:

```ts
let { name = $bindable() } = $props();
```

...estamos permitiendo que `name` se pueda *mutar desde el hijo* y que los cambios viajen hacia el padre, logrando un **two-way binding** completo usando `bind:name` en el padre.

## 🧪 Componentes

### `Parent.svelte`
- Define la variable `name`
- Muestra su valor
- Renderiza `ChildA` y `ChildB` con `bind:name`

### `ChildA.svelte` y `ChildB.svelte`
- Reciben `name` con `$bindable()`
- Cada uno tiene un input que modifica el valor

## 🗣️ Resultado

Cambiar el valor en cualquiera de los inputs (A o B) actualiza la variable en el padre, lo cual a su vez actualiza a ambos hijos. ¡Una sincronización total!

Ideal para entender cómo fluye la reactividad entre componentes en Svelte 5.

---
> *PD: El concepto que buscabas es "two-way binding" (enlace bidireccional). En castellano sería algo así como "sincronización de doble vía".*
