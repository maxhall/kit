<script>
	import { page } from '$app/stores';
	import { onMount } from 'svelte';

	/** @type {string} */
	let hash

	onMount(set_hash);

	function set_hash() {
		hash = window.location.hash;
	}
</script>

<svelte:window on:hashchange={set_hash} />

<h1 id="window-hash">{hash}</h1>
<h1 id="page-url-hash">{$page.url.hash}</h1>

<a href="#target">Nav to #ing with anchor tag</a>
<div id="target">Target</div>
