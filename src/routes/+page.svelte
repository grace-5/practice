<script lang="ts">
    import PopGoes from '../lib/components/PopGoes.svelte';  
    import TextBox from '../lib/components/TextBox.svelte'; 
	import FactList from '../lib/components/FactList.svelte';
</script>
<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>
<p>hello hello hello hello!</p>

<PopGoes propCount=5 onpop={() => {alert("pop")}} ></PopGoes>

<TextBox></TextBox>

<FactList></FactList>



