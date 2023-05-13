<script>
    import { onMount } from 'svelte';

	const url = import.meta.env.PROD ? 'hello' : "http://localhost:3030/myapp/hello/svelte";

    let greeting = "";

    async function getConfig() {
        const opts = {
            method: "get"
        };
        const response = await fetch(url, opts);
        const result = await response.text();
        console.log("Result:", result);

        greeting = result;
    }

    onMount(() => getConfig())
</script>

<h1>{greeting}</h1>