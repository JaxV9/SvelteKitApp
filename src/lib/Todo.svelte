<script lang="ts">

export let tasksProps : Array<string> = [];
    
    let newtask: string = "";

    const increment = (newtask: string) => {
        tasksProps = [...tasksProps, newtask]
        newtask = "";
    }

    const deleteTask = (index: number) => {
        let itemId = tasksProps.findIndex((task, id) => id === index);
		tasksProps.splice(itemId,1);
		tasksProps = tasksProps;
    }
    
</script>
    
<h2>Todo</h2>

<form>
    <input type="text" bind:value="{newtask}">
    <button type="button" on:click={()=>increment(newtask)}>Ajouter</button>
</form>

<ul>
    {#each tasksProps as task, index}
        <li>{tasksProps[index]}</li><button on:click={() => deleteTask(index)}>Delete</button>
    {/each}
</ul>

<slot />


<style>

</style>