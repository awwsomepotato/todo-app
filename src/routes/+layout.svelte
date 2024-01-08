<script lang="ts">
    import "../app.css";
    import Navbar from "$lib/components/Navbar.svelte"
</script>

<div id="everything"
class="flex flex-col md:flex-row h-screen w-screen items-center text-subtext0">

    <Navbar/>

    <div class="w-full h-full flex flex-col sm:p-3">
        <slot/>
    </div>

</div>