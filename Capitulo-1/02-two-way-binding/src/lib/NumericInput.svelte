<script>
  let { value = $bindable(), title = "Undefined title" } = $props();
</script>

<div class="card">
  <h3>{title}</h3>
  <label style="display: flex; justify-content: center; gap: 1em">
    <input type="number" bind:value min="0" max="10" />
    <input type="range" bind:value min="0" max="10" />
  </label>
</div>
