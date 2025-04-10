# 🥋 Capítulo 1 — Introducción - Two-way Binding en Svelte 5

Este capítulo del **Dojo Svelte** se centra en comprender y dominar el **enlace bidireccional** (`two-way binding`) entre componentes usando las nuevas **runes** de Svelte 5.

Aprenderás a sincronizar datos entre componentes padres e hijos, utilizando inputs de diferentes tipos para reflejar los cambios en tiempo real.

---

## 🧠 Conceptos clave

- 🌀 `$bindable()` y `bind:` para lograr reactividad bidireccional
- Comunicación entre componentes padre e hijo
- Manejo de formularios y entradas reactivas
- Composición de componentes reutilizables (`TextInput`, `RadioGroup`, etc.)

---

## 🧪 Componentes explorados

| Componente      | Descripción                                                             |
| --------------- | ----------------------------------------------------------------------- |
| `TextInput`     | Input de texto básico con binding reactivo                              |
| `NumericInput`  | Input numérico y deslizadores sincronizados (`type="number"` y `range`) |
| `CheckboxInput` | Toggle booleano con estado compartido                                   |
| `CheckboxGroup` | Grupo de checkboxes con selección múltiple (`bind:group`)               |
| `SingleSelect`  | Selector `<select>` de un solo valor (`bind:value`)                     |
| `MultiSelect`   | Selector múltiple con mejor estilo personalizado                        |
| `RadioGroup`    | Radios sincronizados con opción única seleccionada                      |
| `TextAreaInput` | Área de texto con binding                                               |

---

## 🧩 Katas implementadas

- `KataTextInputBind`
- `KataNumericInputBind`
- `KataCheckboxInputBind`
- `KataCheckboxGroupBind`
- `KataSelectLabelKeyBind`
- `KataSelectGetLabelBind`
- `KataSelectMultipleBind`
- `KataRadioGroupBind`
- `KataTextAreaInputBind`

Cada kata es una pantalla independiente dentro del proyecto donde se entrena un tipo específico de input y su comportamiento con **props reactivas**.

---

## 📦 Organización

```bash
src/
│
├── lib/          # Componentes reutilizables (inputs, selects, etc.)
├── screen/       # Katas individuales que muestran cada caso de binding
└── app.svelte    # Punto de entrada que muestra las pantallas activas
```

---

## 🔥 ¿Qué te llevás?

Al finalizar este capítulo vas a:

- Comprender el funcionamiento interno del binding bidireccional con `$bindable()`
- Saber cómo construir componentes reusables y composables
- Poder integrar diferentes tipos de entrada en formularios reactivos
- Tener una base sólida para avanzar hacia formularios complejos y validaciones

---
