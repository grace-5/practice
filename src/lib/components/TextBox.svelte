<script lang="ts">
    let text = $state('Your Name Here');
</script>

<hr>
<pre>{text}</pre>
<div bind:textContent={text} contenteditable></div>

<style>
	[contenteditable] {
		padding: 0.5em;
		border: 1px solid #eee;
		border-radius: 4px;
	}
</style>
<hr>