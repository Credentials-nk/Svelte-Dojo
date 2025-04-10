<script lang="ts">
  import RadioGroup from "../lib/RadioGroup.svelte";
  import type { Team } from "../interfaces/Team.interface";
  import teams from "../data/teams.json";
  import CheckboxGroup from "../lib/CheckboxGroup.svelte";

  let selectedIds = $state<number[]>([]);
</script>

<div class="card" style="padding: 1rem;">
  <h4>Parent Component</h4>
  <span>
    Selected: {selectedIds
      .map((id) => teams.find((team) => team.id === id)?.country)
      .filter(Boolean)
      .join(" - ")}
  </span>

  <hr />

  <div
    style="display: flex; flex-direction: column; align-items: flex-start; gap: 0.5rem; padding: 0 6rem;"
  >
    <CheckboxGroup
      options={teams}
      getLabel={(team: Team) => `${team.country} ${team.emoji}`}
      bind:selectedIds
      name="team"
    />
  </div>
</div>
