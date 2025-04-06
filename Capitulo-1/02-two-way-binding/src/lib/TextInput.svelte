<script lang="ts">
    let { name = $bindable(), title='Undefined title' } = $props();
  </script>
  
  <div class="card">
    <h3>{title}</h3>
    <input bind:value={name} placeholder={`Edit from ${title}...`} />
  </div>
  