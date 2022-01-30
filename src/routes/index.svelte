<script lang="typescript">
    let number: number = 5;

    const increament = () => {
        number ++;
    }
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<button on:click={increament}>{number}</button>

