<script lang="ts">
  import Counter from './lib/Counter.svelte';
  import CustomCounter from './lib/CustomCounter.svelte';
  import MiniCounter from './lib/MiniCounter.svelte';
  import Tecnologies from './lib/Tecnologies.svelte';

  let count = $state(0);
</script>

<main>
  <Tecnologies />

  <h3>Counter App</h3>

  <div class="card">
    <p>State en el componente padre: {count}</p>
    <Counter increment={2} decrement={1} on:step={e => (count += e.detail)} />
  </div>

  <div class="card">
    <MiniCounter />
  </div>

  <div class="card">
    <CustomCounter inc={2} dec={1} />
  </div>
</main>
