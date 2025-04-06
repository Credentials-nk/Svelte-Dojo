<script lang="ts">
  import TextInput from "../lib/TextInput.svelte";

  let name = "";
</script>

<main>
  <div class="card">
    <h4>Parent Component</h4>
    <p>Name in parent: {name}</p>
  </div>

  <div
    style="display: flex; gap: 1em; align-items: flex-start; border: 1px solid #ccc; padding: 1rem; border-radius: 8px;"
  >
    <TextInput title="Child A" bind:name />
    <TextInput title="Child B" bind:name />
  </div>
</main>
