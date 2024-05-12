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

  <div class="buttons">
    <Button size="lg" class="Down__Button"><ArrowDownOutline /></Button>
    <Button size="lg" class="Up__Button"><ArrowUpOutline /></Button>
    <Button size="lg" class="Left__Button"><ArrowLeftOutline /></Button>
    <Button size="lg" class="Right__Button"><ArrowRightOutline /></Button>
  </div>
</div>

<style>
  .wrapper{
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

  .buttons{
    display: flex;
    grid-column: 1;
    grid-row: 2;
    justify-content: center;
    align-items: center;
  }

</style>