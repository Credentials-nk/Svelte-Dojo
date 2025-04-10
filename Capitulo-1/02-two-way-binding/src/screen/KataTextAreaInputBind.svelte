<script lang="ts">
  import TextAreaInput from "../lib/TextAreaInput.svelte";

  let value = $state("");
</script>

<div class="card">
  <h4>Parent Component</h4>
  <p>Output in parent</p>

  <textarea>{value}</textarea>
</div>

<div class="card">
  <TextAreaInput title="Box area" bind:value />
</div>
