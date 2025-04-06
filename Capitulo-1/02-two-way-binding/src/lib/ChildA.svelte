<script lang="ts">
  let { name = $bindable() } = $props();
</script>

<div class="card">
  <h3>Child A</h3>
  <input bind:value={name} placeholder="Edit from A" />
</div>
