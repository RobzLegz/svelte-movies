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
    @import url("https://fonts.googleapis.com/css2?family=Roboto&display=swap");

    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: "Roboto", sans-serif;
    }

    .movie-card{
        width: 200px;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: flex-start;
    }

    img{
        width: 100%;
        height: 300px;
        object-fit: cover;
        border-radius: 1rem;
    }

    h3{
        font-size: 16px;
        margin: 10px 0;
    }

    p{
        color: #b9b9b9;
        font-size: 12px;
    }
</style>