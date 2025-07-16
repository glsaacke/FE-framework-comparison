<script lang="js">
    let newTask = $state("")
    let {addTask} = $props()

    function formSubmitted(e){
        e.preventDefault()
        addTask()
        newTask = ""
    }
</script>

<form onsubmit={formSubmitted}>
    <label>
        Task
        <input name="newTask" bind:value={newTask}>
    </label>
    <div class="button-container">
        <button>Add</button>
    </div>
    
</form>

<style>
    form{
        
    }
    .button-container {
        display: flex;
        justify-content: end;
    }
</style>