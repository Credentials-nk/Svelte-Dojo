<script lang="ts">
  import RadioGroup from "../lib/RadioGroup.svelte";
  import type { Team } from "../interfaces/Team.interface";
  import teams from "../data/teams.json";

  let selected = $state<Team>();
</script>

<div class="card" style="padding: 1rem;">
  <h4>Parent Component</h4>
  <span>Selected: {selected?.country}</span>
  <hr />

  <div
    style="display: flex; flex-direction: column; align-items: flex-start; gap: 0.5rem; padding: 0 6rem;"
  >
    <RadioGroup
      options={teams}
      getLabel={(team: Team) => `${team.country} ${team.emoji}`}
      bind:selected
      name="team"
    />
  </div>
</div>
