<script>
	import SingleEntry from '../../components/blender/singleEntry.svelte';
	import { sortedDocumentationData } from '../../data/blender/documentationData';
</script>

<svelte:head>
	<title>Blender Hotkey Documentation</title>
</svelte:head>

<div class="mainContainer">
	<h1 class="ms-2">This is a blender documentation</h1>
	<div>
		{#each sortedDocumentationData as entry (entry.name)}
			<SingleEntry name={entry.name} description={entry.description} keystroke={entry.keystroke} />
		{/each}
	</div>
</div>

<style>
	.mainContainer {
		width: 85%;
		margin-left: 15%;
		transition: all 0.1s;
	}

	@media only screen and (max-width: 1200px) {
		.mainContainer {
			width: 100%;
			margin-left: 0;
		}
	}
</style>
