<script 
    lang="ts"
    context="module"
>
    const load = async ({fetch}) => {
        const res = await fetch(`https://api.themoviedb.org/3/movie/popular?api_key=${import.meta.env.VITE_TMDB_API_KEY}&language=en-US&page=1`);

        if(!res.ok){
            return "lol";
        }

        const data = await res.json();

        return {
            props: {
                movies: data.results
            }
        }
    }

    export {
        load
    }; 
</script>

<script lang="ts">
    import MovieContainer from "../components/movieContainer.svelte";

    import type { Movie } from "../types/interfaces";

    let movies: Movie[];

    export {
        movies
    }
</script>

<MovieContainer movies={movies} />