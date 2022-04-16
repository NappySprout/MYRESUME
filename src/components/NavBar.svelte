
<script>
    import Home from "../pages/Home.svelte";
    import About from "../pages/About.svelte";
    import Experience from "../pages/Experience.svelte";
    let pageid = 0;
    export const navOptions = [
        {page:"Home", component:Home},
        {page:"About", component:About},
        {page:"Experience", component:Experience}
    ]

const handleNav = (e) => {
    console.log(e.srcElement.id)
    pageid = e.srcElement.id }



</script>

<nav class="grid">
    {#each navOptions as x,i}
    <span on:click={handleNav} id={i.toString()}>{x.page}</span>
    {/each}
</nav>
<svelte:component this={navOptions[pageid].component}/>
<style>
    .grid {
        display: grid;
        grid-template-columns: auto auto auto;
        padding:2em;
    }
    span {
        text-align: center;
        
    }
</style>