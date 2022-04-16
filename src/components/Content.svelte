<script>
    export let text;

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
<div class:hidden bind:this={el}>
<p>
    {text}
</p>
</div>

<style>
    p{
        padding:2em 5em 5em;
        font-size: 1.5em;
        text-align: left;
        font-family: monospace;
    }
    div{
        display:inline-block;
        width:55em;   
        opacity:1;
        transition:opacity 1000ms linear;
    }
    .hidden {
        opacity:0;
    }
</style>