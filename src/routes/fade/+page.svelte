<script lang="ts">
	import { fade } from 'svelte/transition';
	let visible = true;
</script>

{#if visible}
	<div class="fade-container" transition:fade>Fade me in and out</div>
{/if}

<button on:click={() => (visible = !visible)}> Toggle Visibility </button>

<style>
	.fade-container {
		padding: 20px;
		margin: 50px;
		background-color: lightcoral;
		color: white;
		border-radius: 8px;
		text-align: center;
		width: 200px;
		margin-left: auto;
		margin-right: auto;
	}

	button {
		display: block;
		margin: 20px auto;
		padding: 10px 20px;
		border: none;
		border-radius: 5px;
		background-color: lightskyblue;
		color: white;
		cursor: pointer;
		font-size: 16px;
	}

	button:hover {
		background-color: deepskyblue;
	}
</style>
