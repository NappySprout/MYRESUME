<script>
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
    export let text;





</script>
<h1 bind:this={el} class:hidden>
    {text}
</h1>

<style>
    h1{
        padding:2em 0em 1em;
        font-size: 3em;
        font-family: monospace;
        opacity:1;
        transition:opacity 1000ms linear;
    }
    .hidden {
        opacity:0;
    }
</style>