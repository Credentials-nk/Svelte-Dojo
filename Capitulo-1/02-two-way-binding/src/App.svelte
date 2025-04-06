<script lang="ts">
  import Tecnologies from "./lib/Tecnologies.svelte";
  import KataCheckboxInputBind from "./screen/KataCheckboxInputBind.svelte";
  import KataNumericInputBind from "./screen/KataNumericInputBind.svelte";
  import KataTextInputBind from "./screen/KataTextInputBind.svelte";

  let name = "Niko";
</script>

<main>
  <Tecnologies />
  <h2 style="text-align: center;">🧪 Kata: Two-way Binding via Prop</h2>

  <!-- <KataTextInputBind /> -->

  <!-- <KataNumericInputBind /> -->

  <KataCheckboxInputBind />
</main>
