<script>
    import Breathe from "../components/Breathe.svelte"
    import Header from "../components/Header.svelte"
    import SubHeader from "../components/SubHeader.svelte"
    import Content from "../components/Content.svelte"
</script>
<main>
    <div>
    <Breathe text="Experience"/>
    </div>
    <Header text="Software Dev Intern @ Delvify"/>
    <SubHeader text="FEBRUARY 2021 - AUGUST 2021"/> 
    <Content text="project deployment with AWS, fulls-stack web app dashboard with authentication using JWT, React, Redux on the frontend, Nodejs express server with PSQL backend, used AWS services such as S3 buckets, load balancer, ECS"/> 
    <Header text="Personal Projects"/>
    <SubHeader text="Multiplayer game" url="https://nappysprout.github.io/boxheadmulti/"/> 
    <Content text="Built a multiplayer game with pure HTML, CSS, JS with no framework on the frontend, backend using socket.io, deployed on heroku. Proficient with javascript even without a framework like Svelte or React."/>
    <SubHeader text="Conway's Game of Life / Cellular Automata" url="https://nappysprout.github.io/Cells/"/> 
    <Content text="Used HTML canvas, pure HTML CSS JS, contains  Conway's Game of Life. another setting to create organic looking bulges on the screen with a different cellular automata setting"/>
</main>
<style>
    main{
        text-align: center;
    }
    div{
        padding:12em;
    }


</style>