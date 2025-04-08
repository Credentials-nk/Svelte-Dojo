<script lang="ts">
  import SingleSelectGetLabel from "../lib/SingleSelectGetLabel.svelte";
  import type { Team } from "../interfaces/Team.interface";

  import teams from "../data/teams.json";

  let selected = $state<Team>();
</script>

<div class="card">
  <h4>Parent Component</h4>
  <p>Country in parent: {selected?.country ?? ""}</p>
  <p>Coups in parent: {selected?.emoji ?? ""}</p>
</div>

<div
  style="display: flex; gap: 1em; align-items: flex-start; border: 1px solid #ccc; padding: 1rem; border-radius: 8px;"
>
  <SingleSelectGetLabel
    options={teams}
    getLabel={(team: Team) => `${team.country} ${team.emoji}`}
    bind:selected
  />
</div>
