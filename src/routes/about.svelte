<script context="module">
	import { browser, dev } from '$app/env';
	// @ts-ignore
	import Contact from '$lib/Contact.svelte';

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;
</script>

<script>
	// @ts-ignore
	import Members from '$lib/Members.svelte';
</script>

<svelte:head>
	<title>About</title>
</svelte:head>

<div class="content">
	<h1>About the Otranto Civic Club</h1>
	<Contact />
	<Members />
</div>

<style>
	.content {
		width: 100%;
		max-width: var(--column-width);
		margin: var(--column-margin-top) auto 0 auto;
	}
</style>
