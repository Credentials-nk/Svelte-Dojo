<script lang="ts">
  let { checked = $bindable() } = $props();
</script>

<div class="card">
  <label>
    <input type="checkbox" bind:checked />
    Yes! Send me regular email spam
  </label>
</div>
