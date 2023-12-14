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
                <div class="m-2">
                <div>{theme}</div>
                </div>
            {/each}
        </div>
    </div>
</main>

<style (lang="postcss")>

    @media (min-width: 768px) {

    }

</style>