<script lang="ts">
    import type { Movie } from "../types/interfaces";
    import MovieCard from "./MovieCard.svelte";

    let movies: Movie[];

    export {
        movies
    }
</script>

<h3>popular</h3>

<div class="movies">
    {#each movies as movie}
        <MovieCard movie={movie} />
    {/each}
</div>

<style>
    .movies{
        widows: 100%;
        display: grid;
        grid-template-columns: repeat(autofit, minmax(250px, 1fr));
        column-gap: 1rem;
        row-gap: 2rem;
    }
</style>