<script>
	import { fade, fly } from 'svelte/transition';
	import Breathe from "../components/Breathe.svelte"
</script>


	<main in:fly="{{ y: 50, duration: 500, delay: 400 }}" out:fly="{{ y: 50, duration: 500 }}">
		<Breathe text="Hello World" padding="5em"/>
		<div class="fixed"><p class="fade2000 pop">Personal Svelte site of Darie Chan Rong Zhi</p></div>
	</main>

<style>
	.fixed {
		height : 2em;
	}

	p { 
		padding:2em;
	}

	main {
		text-align: center;
	}

	.fade2000, .pop{
		animation: fade-in-load 2000ms ease-in;
		transition: font-size 500ms ease-in-out;
	}
	.pop:hover {
		font-size: 1.1em;
	}
	@keyframes fade-in-load {
		0% {
			opacity: 0;
		}
		50% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}
</style>