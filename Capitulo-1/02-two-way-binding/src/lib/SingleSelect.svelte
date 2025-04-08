<script>
  let { selected = $bindable(), options, labelKey = "label" } = $props();
</script>

<select bind:value={selected}>
  {#each options as option}
    <option value={option}>
      {option[labelKey]}
    </option>
  {/each}
</select>
