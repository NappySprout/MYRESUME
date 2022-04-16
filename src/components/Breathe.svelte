<script>
    export let text ;
    export let padding;
</script>
<h1 class="breathe" style="--padding:{padding}">{text}</h1>
<style>
    h1 {
        padding: var(--padding);
		font-size: 3em;
        text-align: center;
    }
        .breathe {
		font-variation-settings: "wght" 100, "wdth" 85;
		animation: breathe 5000ms forwards;
	}

    @keyframes breathe {
		100% {
			font-variation-settings: "wght" 700, "wdth" 200;
		}
	}
</style>