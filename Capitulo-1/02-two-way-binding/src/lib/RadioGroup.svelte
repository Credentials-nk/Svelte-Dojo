<script lang="ts">
  interface Option {
    [key: string]: any;
  }

  let {
    selected = $bindable(),
    options,
    getLabel = (item: Option) => item.label,
    name = "",
  } = $props();
</script>

{#each options as option}
  <label>
    <input type="radio" {name} value={option} bind:group={selected} />
    {getLabel(option)}
  </label>
{/each}
