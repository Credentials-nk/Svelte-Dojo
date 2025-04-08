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

<select bind:value={selected}>
  {#each options as option}
    <option value={option}>
      {getLabel(option)}
    </option>
  {/each}
</select>
