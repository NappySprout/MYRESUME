<script>
    //https://stackoverflow.com/questions/23583245/add-transition-while-changing-img-src-with-javascript
    export let srcs = [];
    export let index = 0;
</script>

<div id= "crossfade">
    {#each srcs as src, i}
    <img {src} alt="pic" class="{index === i ? '' : 'hidden'}" />
    {/each}
</div>

<style>
    #crossfade {
        height:25em;
        position: relative;
        padding:2em;
    }

    img {
        position:absolute;
        margin-left: auto;
        margin-right: auto;
        left: 0;
        right: 0;
        width:25em;
        height:25em;
        border-radius: 50%;
        object-fit: cover;
        transition:opacity 0.5s linear;
    }

    .hidden {
        opacity:0;
    }

</style>
