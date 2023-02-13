<script>
    export let count = 0;
    let step = 1;

    function increment() {
        count += step;
    }

    function decrement() {
        count -= step;
    }

</script>

<svelte:head>
    <title>Counter App</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
</svelte:head>

<main>
<p>count is: {count}</p>

<button on:click={increment}>
    +{step}
</button>

<button on:click={decrement}>
    -{step}
</button>

<p> Change step value: </p>
<input
    type=range
    min=1
    max=10
    bind:value={step}
>

{#if count === 69}
    <p>nice</p>
{/if}

</main>

<style>
    :root {
        display: flex;
        width: 100%;
        justify-content: center;
    }

    main {
        display:flex;
        width: 100%;
        flex-flow: column nowrap;
        justify-content: center;
    }
</style>