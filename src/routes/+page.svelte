<script>
    export let data;
</script>


<body class="flex flex-col text-slate-200 content-center">
    <div class="flex flex-col text-inherit content-center">
        <h1 class="text-inherit text-3xl self-center">
            Welcome to Finnegan's To-Do app
        </h1>
        <p class="text-inherit text-lg self-center">
            {data.visited ? 'Hello!' : 'Click the todo icon in the navbar to get started'}
        </p>
    </div>
</body>

