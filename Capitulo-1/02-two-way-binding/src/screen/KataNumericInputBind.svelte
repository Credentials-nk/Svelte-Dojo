<script lang="ts">
  import NumericInput from "../lib/NumericInput.svelte";
  let value1 = $state(0);
  let value2 = $state(0);
</script>

<div class="card">
  <h4>Parent Component</h4>
  <p>Result in parent: {value1} + {value2} = {value1 + value2}</p>
</div>

<div
  style="display: flex; gap: 1em; align-items: flex-start; border: 1px solid #ccc; padding: 1rem; border-radius: 8px;"
>
  <NumericInput title="Child A" bind:value={value1} />
  <NumericInput title="Child 2" bind:value={value2} />
</div>
