<script>
	import Counter from '$lib/Counter.svelte';

	let user = { loggedIn: false };

	function toggle() {
		user.loggedIn = !user.loggedIn;
	}
</script>

<template lang="pug">
	main
		h1 Pug+Svelte: Else-if Logic Blocks
		
		p
			| How to 
			a(href="https://github.com/sveltejs/svelte-preprocess/blob/main/docs/preprocessing.md#pug") use Pug in Svelte

		p
			| Compare to 
			a(href="https://svelte.dev/tutorial/else-blocks") original example in HTML

		+if('user.loggedIn')
			p: button(on:click='{toggle}') Log out
			p: Counter
			+else
				p: button(on:click='{toggle}') Log in

</template>

<style>
	main {
		text-align: center;
		padding: 1em;
		margin: 0 auto;
	}
</style>


