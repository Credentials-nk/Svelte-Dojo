<script lang="ts">
  import Tecnologies from "./lib/Tecnologies.svelte";
  import KataCheckboxGroupBind from "./screen/KataCheckboxGroupBind.svelte";
  import KataCheckboxInputBind from "./screen/KataCheckboxInputBind.svelte";
  import KataNumericInputBind from "./screen/KataNumericInputBind.svelte";
  import KataRadioGroupBind from "./screen/KataRadioGroupBind.svelte";
  import KataSelectGetLabelBind from "./screen/KataSelectGetLabelBind.svelte";
  import KataSelectLabelKeyBind from "./screen/KataSelectLabelKeyBind.svelte";
  import KataSelectMultipleBind from "./screen/KataSelectMultipleBind.svelte";
  import KataTextAreaInputBind from "./screen/KataTextAreaInputBind.svelte";
  import KataTextInputBind from "./screen/KataTextInputBind.svelte";

  let name = "Niko";
</script>

<main>
  <Tecnologies />
  <h2 style="text-align: center;">🧪 Kata: Two-way Binding via Prop</h2>

  <!-- <KataTextInputBind /> -->

  <!-- <KataNumericInputBind /> -->

  <!-- <KataCheckboxInputBind /> -->

  <!-- <KataSelectLabelKeyBind /> -->

  <!-- <KataSelectGetLabelBind /> -->

  <!-- <KataRadioGroupBind /> -->

  <!-- <KataCheckboxGroupBind /> -->

  <!-- <KataSelectMultipleBind /> -->

  <KataTextAreaInputBind />
</main>
