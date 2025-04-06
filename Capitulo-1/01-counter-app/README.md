
# Svelte Counter Examples

This project contains three different counter implementations using Svelte, each demonstrating a progressively more decoupled architecture and a different approach to state management.

---

## 📦 1. Basic Counter (Internal State)

This component maintains its own state and exposes only the visual representation and buttons to the parent. All state updates happen internally.

- ➕ Increments by 1  
- ➖ Decrements by 1  
- No props or events used

**Usage:**
```svelte
<script>
  import BasicCounter from './BasicCounter.svelte';
</script>

<BasicCounter />
```

---

## 🛠️ 2. Configurable Counter (Props, Internal State)

This version allows the parent to define how much the counter should increment or decrement by, using props. However, the state is still internal to the component.

- Props:
  - `increment` (default: 1)
  - `decrement` (default: 1)

**Usage:**
```svelte
<script>
  import ConfigurableCounter from './ConfigurableCounter.svelte';
</script>

<ConfigurableCounter increment={5} decrement={2} />
```

---

## 📤 3. Decoupled Counter (Events, External State)

This is the most advanced example. The component only emits events (`on:change`) with the increment/decrement value in the event `detail`. The state is fully managed by the parent component.

- Emits:
  - `change` event with `{ detail: number }`

**Usage:**
```svelte
<script>
  import EventCounter from './EventCounter.svelte';

  let count = 0;

  function handleChange(event) {
    count += event.detail;
  }
</script>

<EventCounter on:change={handleChange} />

<p>Count: {count}</p>
```

---

## 🧠 Purpose

These examples are meant to help understand how to:

- Manage local vs. global state
- Pass props to components
- Emit and handle custom events
- Build reactive UIs in Svelte with clear boundaries of responsibility

---

Enjoy building with Svelte! 🚀
