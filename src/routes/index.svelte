<script 
    lang="typescript"
    context="module"
>
    const API_KEY = "123";

    const load = async ({fetch}) => {
        const res = await fetch(`https://api.themoviedb.org/3/movie/popular?api_key=${API_KEY}&language=en-US&page=1`);

        if(!res.ok){
            return "lol";
        }

        const data = await res.json();

        return {
            props: {
                popular: data.results
            }
        }
    }

    export {
        load
    }; 
</script>

<script lang="typescript">
    import MovieContainer from "../components/movieContainer.svelte";

    import type { Movie } from "../types/interfaces";

    let popular: Movie[];

    export {
        popular
    }
</script>

<MovieContainer movies={popular} />