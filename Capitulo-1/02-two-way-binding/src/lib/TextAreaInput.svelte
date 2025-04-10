<script lang="ts">
  let { value = $bindable(), title = "Undefined title" } = $props();
</script>

<div class="card">
  <h3>{title}</h3>
  <textarea bind:value></textarea>
</div>
