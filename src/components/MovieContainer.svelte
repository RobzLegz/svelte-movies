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
    @import url("https://fonts.googleapis.com/css2?family=Roboto&display=swap");

    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: "Roboto", sans-serif;
    }

    h3{
        font-size: 20px;
        font-family: "Roboto", sans-serif;
    }

    .movies{
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        column-gap: 1rem;
        row-gap: 2rem;
    }
</style>