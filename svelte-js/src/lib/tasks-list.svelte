<script>
    let {tasks} = $props()
</script>

<section>
    {#each tasks as task}
      <article>
        {task.title}
      </article>
    {/each}
  </section>