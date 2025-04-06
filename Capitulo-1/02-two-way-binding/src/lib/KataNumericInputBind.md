# 🧪 Kata: Two-way Binding with Numeric Inputs

Este kata demuestra cómo sincronizar dos valores numéricos entre un componente padre y dos hijos usando `bind:value` con `<input type="number">` y `<input type="range">`.

---

### 🧠 Concepto clave

En Svelte 5 con runes, podemos declarar props bindables así:

```ts
let { value = $bindable(), title = "Undefined title" } = $props();
```

Esto permite que el componente padre controle la variable `value`, y que los hijos puedan modificarla y reflejar los cambios en tiempo real.

---

### 📦 Componentes involucrados

| Componente              | Función                                             |
|--------------------------|-----------------------------------------------------|
| `KataNumericInputBind`   | Componente principal que define `value1` y `value2` |
| `NumericInput`           | Input doble (número + slider) que modifica un valor |

---

### ⚙️ ¿Qué sucede?

- El padre define dos estados numéricos: `value1` y `value2`
- Los pasa como props bindables a dos `NumericInput`
- Cada `NumericInput` permite modificar su valor a través de un campo numérico y un slider
- El padre escucha esos cambios y muestra el resultado de la suma en tiempo real

---

### 🧩 Código clave en el padre

```ts
let value1 = $state(0);
let value2 = $state(0);
```

```svelte
<NumericInput title="Child A" bind:value={value1} />
<NumericInput title="Child B" bind:value={value2} />
```

---

### 🧮 Resultado

> Result in parent: **6 + 3 = 9**

Al modificar cualquiera de los hijos, la suma en el padre se actualiza sin necesidad de lógica adicional. Una forma clara de visualizar cómo funciona el `bind:` bidireccional con tipos numéricos.
