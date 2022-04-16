<script>
    import Breathe from "../components/Breathe.svelte"
    import CrossFade from "../components/CrossFade.svelte"
    const content = "My name is Darie Chan, loves guitar, dance and"
    import { fade, fly } from 'svelte/transition';
    let originsrc = './images/me.jpeg'; let hackersrc = 'https://i.kym-cdn.com/entries/icons/mobile/000/021/807/ig9OoyenpxqdCQyABmOQBZDI0duHk2QZZmWg2Hxd4ro.jpg';
    let srclist = [originsrc, hackersrc];
    const handleEnter = (e) => index = 1;
    const handleLeave = (e) => index = 0;
    let index = 0;
</script>
<main in:fly="{{ y: 50, duration: 500, delay: 1000 }}" out:fly="{{ y: 50, duration: 500 }}">
    <Breathe text="About" padding="1em 3em 0.5em"/>
    <CrossFade srcs={srclist} {index}/>
    <div>
        <p>{content} 
            <span class="interact" on:mouseenter={handleEnter} on:mouseleave={handleLeave}>"Computer Science"</span>
        </p>
        <p>
            My <a href="https://www.linkedin.com/in/darie-chan-rong-zhi-4301a9207/">Linkedin</a> and my <a href ="https://github.com/NappySprout">Github</a>
        </p>
    </div>
</main>

<style>
    main {
        text-align: center;
    }

    p {
        font-size: 1.5em;
        padding:2em auto 1.7em;
    }


    @keyframes breathe {
		100% {
			font-variation-settings: "wght" 700, "wdth" 200;
		}
	}

    .interact {
        animation: bounce 1s ease-in infinite;
        position:relative;
        display:inline-block;
        color:aquamarine;
    }

    @keyframes bounce {
        0%   { transform: scale(1,1) translateY(0); }
        10%  { transform: scale(1.1,.9) translateY(0); }
        30%  { transform: scale(.9,1.1) translateY(-5px);}
        50%  { transform: scale(1.05,.95) translateY(0); }
        58%  { transform: scale(1,1) translateY(-1px); }
        65%  { transform: scale(1,1) translateY(0);}
        100% { transform: scale(1,1) translateY(0);}
    }
</style>