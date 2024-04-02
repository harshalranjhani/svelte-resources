<script lang="ts">
	import { slide } from 'svelte/transition';
	let show = true;
	let items = ['Apple', 'Banana', 'Cherry'];
</script>

<h1>Hello Svelte!</h1>

{#if show}
	<ul transition:slide>
		{#each items as item}
			<li>{item}</li>
		{/each}
	</ul>
{/if}

<button on:click={() => (show = !show)}>Toggle Visibility</button>

<style>
	h1 {
		color: darkslateblue;
		text-align: center;
	}

	ul {
		list-style-type: none;
		padding: 0;
		margin: 20px auto;
		width: fit-content;
		border-radius: 8px;
		background-color: lavender;
		box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
	}

	li {
		padding: 10px 20px;
		color: darkslategray;
		border-bottom: 1px solid #eee;
	}

	li:last-child {
		border-bottom: none;
	}

	button {
		display: block;
		margin: 20px auto;
		padding: 10px 20px;
		border: none;
		border-radius: 5px;
		background-color: slateblue;
		color: white;
		cursor: pointer;
		font-size: 16px;
		transition: background-color 0.3s ease;
	}

	button:hover {
		background-color: rebeccapurple;
	}
</style>
