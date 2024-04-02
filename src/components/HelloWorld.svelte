<script lang="ts">
	import { onMount, onDestroy } from 'svelte';

	onMount(() => {
		console.log('Component has been mounted');
	});

	onDestroy(() => {
		console.log('Component is being destroyed');
	});

	let name = 'world';
	let num = 0;

	function increment() {
		num += 1;
	}
</script>

<h1>Hello {name}!</h1>
<h2>Number: {num}</h2>
<button on:click={increment}>Increment</button>

<style>
	h1,
	h2 {
		color: royalblue;
		text-align: center;
	}

	h2 {
		margin-top: 0.5rem;
		font-size: 1.25rem;
	}

	button {
		display: block;
		margin: 1rem auto;
		padding: 0.5rem 1rem;
		font-size: 1rem;
		color: white;
		background-color: steelblue;
		border: none;
		border-radius: 5px;
		cursor: pointer;
		transition: background-color 0.2s ease;
	}

	button:hover {
		background-color: dodgerblue;
	}
</style>
