<script>
    import { Palette } from 'lucide-svelte';
    let themes = [
        // dark (t/f), "main color"
        [ true, "Purple" ],
        [ false, "Purple" ],
        [ true, "Pink" ],
        [ false, "Pink"]
    ]
    function themeSwitch() {

    }
</script>

<main class="flex flex-col justify-center content-center text-slate-200 items-center">
    <h1
    class="self-center text-inherit text-xl p-2"
    >Settings</h1>
    <div class="flex flex-col items-center">
        <h1 class=""
        >Theme</h1>
        <Palette/>
        <div class="flex flex-row">     
            {#each themes as theme}
            <button on:click={themeSwitch}
            class="p-1 m-2 flex flex-col items-center">
                {#if theme[0] == true}
                    <h3>dark</h3>
                {:else}
                    <h3>light</h3>
                {/if}
                <h3>{theme[1]}</h3>
            </button>
            {/each}
        </div>
    </div>
</main>

<style (lang="postcss")>

    @media (min-width: 768px) {

    }

</style>