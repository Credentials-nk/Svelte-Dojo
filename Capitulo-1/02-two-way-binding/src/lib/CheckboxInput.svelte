<script lang="ts">
  let { checked = $bindable(), text = "Check me" } = $props();
</script>

<div class="card">
  <label>
    <input type="checkbox" bind:checked />
    {text}
  </label>
</div>
