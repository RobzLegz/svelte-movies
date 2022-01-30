<script lang="ts">
    import type { Movie } from "src/types/interfaces";

    let movie: Movie;

    export {
        movie
    }
</script>

<div class="movie-card">
    <img src={`https://image.tmdb.org/t/p/w300${movie.poster_path}`} alt={`${movie.title} poster`} />

    <h3>{movie.title}</h3>

    <p>{movie.release_date}</p>
</div>

<style>
    .movie-card{
        width: 200px;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: center;
    }

    img{
        width: 100%;
        object-fit: cover;
    }

    h3{
        font-size: 20px;
    }

    p{
        color: #b9b9b9;
        font-size: 16px;
    }
</style>