<script>
  import CheckboxInput from "../lib/CheckboxInput.svelte";

  let yes = $state(false);
</script>

<div class="card">
  <h4>Parent Component</h4>
</div>

<div
  style="display: flex;  align-items: flex-start; border: 1px solid #ccc;  border-radius: 8px;"
>
  <CheckboxInput bind:checked={yes} />
</div>

{#if yes}
  <p>
    Thank you.<br /> We will bombard your inbox and sell your personal details.
  </p>
{:else}
  <p>
    You must opt in to continue. <br />If you're not paying, you're the product.
  </p>
{/if}

<button disabled={!yes}>Subscribe</button>
