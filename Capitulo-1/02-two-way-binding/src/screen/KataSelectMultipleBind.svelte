<script lang="ts">
  import MultiSelect from "../lib/MultiSelect.svelte";
  import teams from "../data/teams.json";
  import type { Team } from "../interfaces/Team.interface";

  let selected = $state<string[]>([]);
</script>

<div class="card">
  <h4>Parent Component</h4>
  <p>Selected:</p>
  <ul>
    {#each selected as name}
      <li>{name}</li>
    {/each}
  </ul>
</div>

<div class="card">
  <MultiSelect
    bind:selected
    options={teams}
    getLabel={(team: Team) => `${team.country}`}
  />
</div>
