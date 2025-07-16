<script lang="js">
  import TasksForm from "./lib/tasks-form.svelte";
  import TasksList from "./lib/tasks-list.svelte";

  let message = "Tasks App"
  let tasks = $state([])

  function addTask(newTask){
    tasks.push({
      id: crypto.randomUUID,
      title: newTask,
      done: false,
    })
  }
</script>

<main>
  <h1>{message}</h1>
  <TasksForm {addTask}/>
  <TasksList {}
</main>

<style>
  main {
    margin: 1rem auto;
    max-width: 800px;
  }
</style>