<script>
	import Navigation from './components/Navigation.svelte';
</script>

<Navigation />
<main>
	<h1>Hello from App.svelte</h1>
</main>

<style type="text/scss">
	$color: red;

	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: $color;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
