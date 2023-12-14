<script>
    import { Plus } from 'lucide-svelte';

    let taskInput = "description goes here"
    let titleInput = "title goes here"
    let date = "Dec 6"

    let tasks = [
        ["Todo", "Dec 6", "this is a todo"],
        ["Todo 2", "Dec 32", "Dec 32?"]
    ];
    let doneTasks = [
        ["Done Todo", "Dec 2", "this is done"]
    ]
    function taskSubmit() {
        tasks.push([titleInput,date,taskInput])
        tasks = tasks;
        console.log(tasks)
        taskInput = "description goes here"
        titleInput = "title goes here"
        date = "Dec 6"
    }
</script>

<body class="text-slate-200 flex flex-col items-center w-full">
    <h1 class="text-3xl self-center text-inherit m-4 text-semibold">
        To-Do App
    </h1>
    <div class="flex flex-col items-center w-4/5 max-w-screen-md min-w-fit">
        <div class="flex flex-col p-2 w-4/5 items-center">
            <div class="task-holder">
                <div class="w-full flex flex-row justify-between p-1 items-center">
                    <input class="w-1/2 rounded-md dark:bg-purple-700 p-1"
                    bind:value={titleInput}/>
                    <div class="flex flex-row p-2">
                    <p>{date}</p>
                    <button class="bg-pink-600 rounded-full w-6.5 h-6.5"
                    on:click={taskSubmit}>
                        <Plus class="w-6.5 h-6.5"/>
                    </button>
                    </div>
                </div>
                <div class="w-full p-1">
                    <input class="w-full rounded-md dark:bg-purple-700   p-1"
                    bind:value={taskInput}/>
                </div>
            </div>
            <div class="w-full flex flex-col-reverse items-center justify-between">
            {#each tasks as task}
                <div class="task-holder">
                <div class="flex flex-row justify-between">
                    <h3 class="p-1"
                    >{task[0]}</h3>
                    <h4 class="p-1"
                    >{task[1]}</h4>
                </div>
                <p class="dark:bg-purple-700 m-1 p-1 rounded-md"
                >{task[2]}</p>
                </div>
            {/each}
            </div>
            <div class="w-full opacity-75 flex flex-col-reverse justify-between">
            {#each doneTasks as task}
                <div class="task-holder self-center">
                <div class="flex flex-row justify-between opacity-75">
                    <h3 class="p-1"
                    >{task[0]}</h3>
                    <h4 class="p-1"
                    >{task[1]}</h4>
                </div>
                <p class="dark:bg-purple-700 m-1 p-1 rounded-md opacity-75"
                >{task[2]}</p>
                </div>
            {/each}
            </div>
        </div>
    </div>
</body>

<style lang="postcss">
    .task-holder {
        @apply dark:bg-purple-800 m-1 p-1 rounded-md w-full
    }
</style>