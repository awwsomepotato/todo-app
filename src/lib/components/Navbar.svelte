<script lang="ts">
    import { Cog, Home, ListTodo, Info } from 'lucide-svelte';
    import { page } from '$app/stores';
    $: currentPage = $page.url.pathname
    if ($page.url.pathname == '/') {

    }
</script>


<header class="navbar">
    <div class="nav-left-contaner">
        <a class="nav-button group {'/' === currentPage ? 'active' : ''} " href='/'>
            <Home class="place-self-center w-6 h-6 md:w-7 md:h-7"/>
            <p class="text-sm self-center">Home</p>
        </a>    
        <a class="nav-button {'/todo' === currentPage ? 'active' : ''}" href='/todo'>
            <ListTodo class="place-self-center w-6 h-6 md:w-7 md:h-7"/>
            <p class="text-sm self-center text-inherit">Todo</p>
        </a>
    </div>
    <div class="nav-right-contaner"> 
        <!--
        <a href="/settings" class="nav-button">
            <Cog class="nav-icon"/>
            <p class="text-sm self-center">Settings</p>
        </a>
        -->
        <a href="/info" class="nav-button {'/info' === currentPage ? 'active' : ''}">
            <Info class="place-self-center w-6 h-6 md:w-7 md:h-7"/>
            <p class="text-sm self-center">Info</p>
        </a>
    </div>
</header>


<style lang="postcss">

    .navbar {
        @apply shadow-md mx-2 my-1 flex flex-row lg:flex-col bg-surface0 justify-between 
        rounded-3xl dark:text-slate-200  h-fit w-[96vw];
    }
    .nav-left-contaner {
        @apply flex flex-row justify-around mx-1 px-1 my-0.5 py-1 text-inherit
    }
    .nav-right-contaner {
        @apply flex flex-col justify-around mx-1 px-2 my-0.5 py-1
    }
    .nav-button {
        @apply relative mx-0.5 px-1 py-0 rounded-xl text-inherit flex flex-col content-center w-12 h-12
    }
    .nav-button.active {
        @apply bg-surface1
    }

    @media (min-width: 768px) {
        .navbar {
            @apply flex-col my-2 mx-1 h-[98vh] w-fit fixed
        }
        .nav-left-contaner {
            @apply flex-col px-0.5 py-1 mx-0.5 my-1
        }
        .nav-right-contaner     {
            @apply my-1 py-1 mx-0.5 px-0.5
        }
        .nav-button {
            @apply my-0.5 mx-2 py-1 px-0 w-14 h-14
        }
    }

</style>