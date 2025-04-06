<script lang="ts">
  let { name = $bindable() } = $props();
</script>

<div class="card">
  <h3>Child B</h3>
  <input bind:value={name} placeholder="Edit from B" />
</div>
