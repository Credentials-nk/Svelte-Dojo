<!-- 
  En este caso este componente se encarga solo de 
  emitir los nuevos valores, que será extraido desde 
  event.detail, pero no modifica, ni conoce el estado 
  que define el componente padre.
-->

<script lang="ts">
  import { createEventDispatcher } from 'svelte';

  interface Props {
    increment: number;
    decrement: number;
  }

  const { increment, decrement }: Props = $props();
  const dispatch = createEventDispatcher();

  function step(delta: number) {
    dispatch('step', delta);
  }
</script>

<button onclick={() => step(-decrement)}>
  -{decrement}
</button>
<span style="margin: 0 12px"></span>
<button onclick={() => step(increment)}>
  +{increment}
</button>
