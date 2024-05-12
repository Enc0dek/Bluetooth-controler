<script>
  import { Button, Card } from "flowbite-svelte";
  import {
    ArrowLeftOutline,
    ArrowRightOutline,
    ArrowUpOutline,
    ArrowDownOutline,
    CogOutline,
  } from "flowbite-svelte-icons";

  var connected = true;
  var buttons = {
    Up: false,
    Down: false,
    Left: false,
    Right: false,
  };
</script>

<div class="wrapper">
  <div class="Status">
    {#if !connected}
      <Card class="text-center bg-red-700">
        <h1 class="text-white mb-2 text-2xl font-bold">
          Bluetooth Disconnected
        </h1>
        <p class="text-white sm:text-lg">Try Conneting to a device</p>

        <Button><CogOutline />Settings</Button>
      </Card>
    {:else}
      <Card class="text-center bg-green-400">
        <h1 class="text-white mb-2 text-2xl font-bold">Connected</h1>
      </Card>
    {/if}
  </div>

  <div
    class="grid justify-items-center gap-2 items-center"
    style="grid-template-columns: 0px 130px 0px; margin: 0 auto;"
  >
    <div class="up__btn">
      <Button class="w-16 h-16"><ArrowUpOutline /></Button>
    </div>
    <div class="left__btn">
      <Button class="w-16 h-16"><ArrowLeftOutline /></Button>
    </div>

    <div class="right__btn">
      <Button class="w-16 h-16"><ArrowRightOutline /></Button>
    </div>

    <div class="down__btn">
      <Button class="w-16 h-16"><ArrowDownOutline /></Button>
    </div>
  </div>
</div>

<style>
  .wrapper {
    display: grid;
    gap: 10px;
  }

  .Status {
    display: flex;
    grid-column: 1;
    grid-row: 1;
    justify-content: center;
    align-items: center;
  }

  .up__btn {
    grid-column: 2;
  }

  .left__btn {
    grid-column: 1;
  }

  .right__btn {
    grid-column: 3;
  }
  .down__btn {
    grid-column: 2;
  }
</style>
