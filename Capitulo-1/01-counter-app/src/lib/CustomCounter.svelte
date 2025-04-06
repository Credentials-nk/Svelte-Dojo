<script lang="ts">
  interface Props {
    inc: number;
    dec: number;
  }

  const { inc, dec }: Props = $props();

  let count = $state(0);

  function changeCount(delta: number) {
    count += delta;
  }
</script>

<div>
  <p>State interno con variación por props</p>
  <button onclick={() => changeCount(-dec)}>-{dec}</button>
  <span style="margin: 0 12px">{count}</span>
  <button onclick={() => changeCount(inc)}>+{inc}</button>
</div>
