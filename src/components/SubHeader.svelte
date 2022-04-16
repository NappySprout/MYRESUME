<script>
    export let text;
    export let url;

    let hidden = false;
    function isInViewport(element) {
        const rect = element.getBoundingClientRect();
        return (
            rect.top >= 0 &&
            rect.left >= 0 &&
            rect.bottom <= (window.innerHeight || document.documentElement.clientHeight) &&
            rect.right <= (window.innerWidth || document.documentElement.clientWidth)
        );
    }
    document.addEventListener("scroll", e => {
        if(isInViewport(el)) {
            hidden = false;
        }
        else {
            hidden =true;
        }
        console.log(hidden)
    }) 
    export let el; 
</script>
<h2 class:hidden bind:this={el}>
    {#if url}
    <a href="url" >{text}</a>
    {:else}
    {text}
    {/if}
    
</h2>

<style>
    h2{
        padding:0em;
        font-size: 1em;
        font-family: monospace;
        opacity:1;
        transition:opacity 1000ms linear;
    }
    a{
        color: aliceblue;
        font-size: 2em;
    }

    .hidden {
        opacity:0;
    }
</style>