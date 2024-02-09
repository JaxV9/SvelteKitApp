<script lang="ts">
    import Fizzbuzz from "$lib/Fizzbuzz.svelte";

    const test:number = 0;

    const numbers = [1, 2, 12, 42]

</script>

    <!-- <Fizzbuzz testProps={test}/> -->

    <Fizzbuzz testProps = {numbers}>
        <p>Test</p>
    </Fizzbuzz>

<style>
    
</style>