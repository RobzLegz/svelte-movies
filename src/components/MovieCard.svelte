<script lang="ts">
    import type { Movie } from "src/types/interfaces";

    let movie: Movie;

    export {
        movie
    }
</script>

<div class="movie-card">
    <img src={`https://image.tmdb.org/t/p/w300${movie.poster_path}`} alt={`${movie.title} poster`} />
</div>