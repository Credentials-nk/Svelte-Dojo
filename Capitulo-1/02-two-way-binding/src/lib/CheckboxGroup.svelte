<script lang="ts">
  interface Option {
    [key: string]: any;
  }

  let {
    selectedIds = $bindable(),
    options,
    getLabel = (item: Option) => item.label,
    name,
  } = $props();
</script>

{#each options as option}
  <label style="margin-bottom: 0.25rem;">
    <input type="checkbox" {name} value={option.id} bind:group={selectedIds} />
    {getLabel(option)}
  </label>
{/each}
