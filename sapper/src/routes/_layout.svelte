<script>
	//import Nav from '../components/nav/index.svelte';
	import Navbar from '../components/navbar/index.svelte'

	export let segment;
</script>

<style>
	main {
		position: relative;
		max-width: 56em;
		background-color: white;
		padding: 2em;
		margin: 0 auto;
		box-sizing: border-box;
	}
</style>

<!-- <Nav {segment}/>-->
<Navbar></Navbar>

<main>
	<slot></slot>
</main>