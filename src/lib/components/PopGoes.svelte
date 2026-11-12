<!-- <svelte:options customElement="pop-goes" /> -->
<script lang="ts">
    import './Stepper.svelte';  

	let count = $state(0);
    let { propCount = 10, onpop=()=>{} } = $props();

	function increment() {
		count++;
        if (count > propCount) {
            count = propCount;
            onpop();
            // $host().dispatchEvent(new CustomEvent("pop"));
        }
	}

</script>

<button onclick={increment}>
	Clicked {count}
	{count === 1 ? 'time' : 'times'}
</button>
<my-stepper
	ondecrement={() => count -= 1}
	onincrement={() => count += 1}
></my-stepper>

<p>count: {count}, propCount: {propCount}</p>