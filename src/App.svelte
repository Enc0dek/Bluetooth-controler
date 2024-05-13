<script>
  import Controler from "./lib/controler.svelte";
  import Toolbar from "./lib/toolbar.svelte";
  import Terminal from "./lib/terminal.svelte";

  var terminalActive = true;

  function switchTerminal() {
    terminalActive = !terminalActive;
  }
</script>

<main class="container">
  <Toolbar {switchTerminal} />
  <Controler />
  <footer>
    {#if terminalActive}
      <Terminal />
    {/if}
  </footer>
</main>
