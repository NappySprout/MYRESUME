<script>
	//https://svelte.dev/repl/ca6de655755d4ae88c4c6cbf60f85fda?version=3.23.0
	import NavBar from "./components/NavBar.svelte";
	
		const x = document.body.addEventListener("mousemove", (e) => {
			document.body.style.backgroundPositionX = -e.clientX * 0.01 + "px";
			document.body.style.backgroundPositionY = -e.clientY * 0.01 + "px";
		});
</script>

	<NavBar/>

<style>
		:global(*, body) {
		padding: 0px;
		margin: 0px;
		color: antiquewhite;
	
	}

	:global(body) {
		background-image: url(https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/022f1ebf-9aed-4121-9152-8eb080328bac/d7dz6nj-31d4b370-c778-4640-a9c7-7e1d56a26f52.png?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzAyMmYxZWJmLTlhZWQtNDEyMS05MTUyLThlYjA4MDMyOGJhY1wvZDdkejZuai0zMWQ0YjM3MC1jNzc4LTQ2NDAtYTljNy03ZTFkNTZhMjZmNTIucG5nIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.L9rgI534l7WPzwFCD-Td9lGHtIbtZrHQL3fu-KLiBho);
		background-size: cover;

	}
</style>