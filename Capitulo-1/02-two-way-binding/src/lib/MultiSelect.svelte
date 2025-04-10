<script lang="ts">
  interface Option {
    [key: string]: any;
  }

  let {
    selected = $bindable(),
    options,
    getLabel = (item: Option) => item.label,
  } = $props();
</script>

<div class="wrapper">
  <label class="wrapper">
    <span class="label">Choose your options</span>
    <select class="multiselect" multiple bind:value={selected}>
      {#each options as option}
        <option>{getLabel(option)}</option>
      {/each}
    </select>
  </label>
</div>

<style>
  .wrapper {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    width: 300px;
  }

  .label {
    font-weight: bold;
    color: white;
  }

  .multiselect {
    background-color: #1e1e1e;
    color: #fff;
    padding: 0.5rem;
    border: 1px solid #444;
    border-radius: 6px;
    font-size: 1rem;
    min-height: 8rem;
    outline: none;
  }

  .multiselect option {
    padding: 0.5rem;
  }

  .multiselect:focus {
    border-color: #7c3aed;
    box-shadow: 0 0 0 2px #7c3aed55;
  }
</style>
