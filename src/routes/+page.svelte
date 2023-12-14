<script>
    export let data;
</script>


<body class="flex flex-col text-text content-center">
    <div class="flex flex-col text-inherit content-center">
        <h1 class="text-inherit text-3xl self-center">
            Welcome to Finnegan's To-Do app
        </h1>
        <p class="text-subtext1 text-xl self-center">
            {data.visited ? 'Hello!' : 'Click the todo icon in the navbar to get started'}
        </p>
    </div>
</body>

