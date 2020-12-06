<script>
	import Header from './Components/Header.svelte';

	export let name;
</script>

<main>
	<Header />

</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: 50rem;
		}
	}
</style>