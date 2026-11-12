<script >
	let facts = $state([]);

	async function getFact() {
		const response = await fetch('https://catfact.ninja/fact');
        try{
            if (response.ok){
                const data = await response.json();
                facts.push(data.fact);
            }
        }
        catch{
            alert("problem!!! get fact");
        }
	}

    getFact();

</script>

<h2>cat facts!!!</h2>

<ul>
    {#each facts as fact}
        <li>
            {fact}
        </li>
    {/each}
</ul>

<button onclick={getFact}>Get more facts!</button>