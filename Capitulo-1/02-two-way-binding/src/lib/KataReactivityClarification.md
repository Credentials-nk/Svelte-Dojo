# 🔍 Apéndice: Reactividad en Svelte 5 – Casos especiales

Este apéndice documenta una distinción importante en el comportamiento de las variables reactivas en Svelte 5.

---

## ✅ Caso 1: Mutación con `$state()` (recomendado)

```ts
let count = $state(0);

function increment() {
  count += 1;
}
```

- `count` es una **señal reactiva**.
- Cualquier cambio se refleja automáticamente en el DOM.
- Ideal para lógica, botones, condiciones, etc.

---

## ⚠️ Caso 2: Mutación sin `$state()` (NO reactivo)

```ts
let count = 0;

function increment() {
  count += 1;
}
```

- El valor cambia internamente, pero el DOM **no lo refleja**.
- No es reactivo porque Svelte no “escucha” cambios en variables comunes.

---

## 🤔 ¿Por qué funciona `bind:checked` con una variable normal?

```ts
let yes = false;
<input type="checkbox" bind:checked={yes} />
```

- El checkbox se actualiza visualmente y cambia el valor de `yes`.
- Si `yes` está **referenciado directamente** en el DOM (ej. `{#if yes}` o `disabled={!yes}`), Svelte recompila el DOM **en ese ciclo**.
- Sin embargo, no es una señal. Si la mutación viene desde otro lugar, **no hay reactividad garantizada**.

---

## 🧠 Conclusión

| Tipo de variable      | DOM se actualiza | Recomendado para lógica |
|------------------------|------------------|---------------------------|
| `$state()`             | ✅ Sí            | ✅ Sí                    |
| `let x = valor` normal | ⚠️ A veces       | ❌ No                    |

---

> Usá `$state()` siempre que quieras asegurar reactividad y claridad en tu aplicación.

