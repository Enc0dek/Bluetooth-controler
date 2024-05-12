<script>
    import { Toolbar, ToolbarGroup, ToolbarButton, Dropdown, DropdownItem } from "flowbite-svelte";
    import { CogOutline, UserOutline} from "flowbite-svelte-icons"
</script>

<div class="wrapper">
    <Toolbar id="Toolbar" class="h-12">
        <ToolbarGroup class="Toolbar__Tittle">
            <p>
                Bluetooth Controler
            </p>
        </ToolbarGroup>

        <ToolbarGroup class="Toolbar__extra">
            <p>
                BY LZ000
            </p>

            <UserOutline/>
        </ToolbarGroup>
        
        <ToolbarButton slot="end"><CogOutline/>
        
        <Dropdown>
            <DropdownItem class="w-36">
                <p>
                    search
                </p>
            </DropdownItem>

            <DropdownItem class="w-36">
                <p>
                    Disconnect
                </p>
            </DropdownItem>

            <DropdownItem class="w-36">
                <p>
                    Terminal
                </p>
            </DropdownItem>
        </Dropdown>

        </ToolbarButton>
    </Toolbar>
</div>

<style>
    .wrapper{
        padding: 10px;
    }

    .Toolbar{
        display: flex;
    }
</style>