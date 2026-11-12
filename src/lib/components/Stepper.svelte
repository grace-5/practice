<!-- Don't recommend component in routes folder! -->
 <svelte:options customElement="my-stepper" />
<script lang="ts">
    function dispatch(type) {
		$host().dispatchEvent(new CustomEvent(type));
	}
</script>
<button onclick={() => dispatch('decrement')}>decrement</button>
<button onclick={() => dispatch('increment')}>increment</button>
<style>
	[contenteditable] {
		padding: 0.5em;
		border: 1px solid #eee;
		border-radius: 4px;
	}
</style>