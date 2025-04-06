<script lang="ts">
  let count = $state(0);
</script>

<div>
  <p>State interno con variación fiaja</p>
  <button onclick={() => count--}>-</button>
  <span style="margin: 0 12px">{count}</span>
  <button onclick={() => count++}>+</button>
</div>
