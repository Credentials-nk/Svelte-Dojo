<script>
  import SingleSelect from "../lib/SingleSelect.svelte";

  import teams from "../data/teams.json";

  let selected = $state();
</script>

<div class="card">
  <h4>Parent Component</h4>
  <p>Country in parent: {selected?.country ?? ""}</p>
  <p>Coups in parent: {selected?.emoji ?? ""}</p>
</div>

<div
  style="display: flex; gap: 1em; align-items: flex-start; border: 1px solid #ccc; padding: 1rem; border-radius: 8px;"
>
  <SingleSelect options={teams} labelKey="country" bind:selected />
</div>
