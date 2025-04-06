<script lang="ts">
  import svelteLogo from './assets/svelte.svg'
  import ChildA from './lib/ChildA.svelte';
  import ChildB from './lib/ChildB.svelte';
  import viteLogo from '/vite.svg'

  let name = 'Niko';
</script>

<main>
  <div>
    <a href="https://vite.dev" target="_blank" rel="noreferrer">
      <img src={viteLogo} class="logo" alt="Vite Logo" />
    </a>
    <a href="https://svelte.dev" target="_blank" rel="noreferrer">
      <img src={svelteLogo} class="logo svelte" alt="Svelte Logo" />
    </a>
  </div>
  <h2>Two way binding</h2>

  <div class="card">
    <h4>Parent Component</h4>
    <p>Name in parent: {name}</p>
  </div>

  <div style="display: flex; gap: 1em; align-items: flex-start; border: 1px solid #ccc; padding: 1rem; border-radius: 8px;">
    <ChildA bind:name />
    <ChildB bind:name />
  </div>
  
  

</main>

<style>
  .logo {
    height: 3em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
</style>
