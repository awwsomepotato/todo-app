<script lang="ts">
    import "../app.css";
    import { Cog, Home, CopyCheck, Moon, Sun } from 'lucide-svelte';
    let dark: boolean = true
    $: console.log(`dark is ${dark}`)
</script>

<div id="everything"
class:dark={dark}
class="flex flex-col md:flex-row h-screen w-screen items-center text-subtext0">
    <header class="navbar">
        <div class="nav-left-contaner">
            <a class="nav-button group" href='/'> 
                <Home class="nav-icon" />
                <p class="text-sm self-center">Home</p>
            </a>
            <a class="nav-button" href='/to-do'>        
                <CopyCheck class="nav-icon text-inherit" />
                <p class="text-sm self-center text-inherit">Todo</p>
            </a>
        </div>
        <div class="nav-right-contaner"> 
            <a href="/settings" class="nav-button">
                <Cog class="nav-icon"/>
                <p class="text-sm self-center">Settings</p>
            </a>
        </div>
    </header>
    <div class="w-full h-full flex flex-col p-3">
        <slot/>
    </div>
</div>

<style (lang="postcss")>

</style>