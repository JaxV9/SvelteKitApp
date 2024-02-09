<script lang="ts">

export let testProps : Array<number> = [];

    let newNumber: number = 0;

    const increment = (newNumber: number) => {
        testProps = [...testProps, newNumber]
        newNumber = 0;
    }

</script>

<h2>Fizzbuzz {testProps}</h2>

<slot />

{#each testProps as number}
    {#if number % 3 === 0 && number % 5 === 0}
        <p>Fizzbuzz</p>
        {:else if number % 3 === 0}
            <p>Fizz</p>
        {:else if number % 5 === 0}
            <p>buzz</p>
        {:else}
            <p>{number}</p>
    {/if}
{/each}

<form>
    <input type="number" bind:value="{newNumber}">
    <button type="button" on:click={()=>increment(newNumber)}>Ajouter</button>
</form>

<style>

</style>