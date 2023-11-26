<script>
    import GithubIcon from "./HeadGithubIcon.svelte";
    import XIcon from "./HeadXIcon.svelte";

    export let current_title="";
</script>

<div class="container">
    <div class:current_title>
        <span>
            {current_title}
        </span>
    </div>
    
    <div class="contact">
        <a class="icon github-icon" href="https://github.com/naosuke884" target="_blank">
            <GithubIcon />
        </a>
        <a class="icon x-icon" href="https://twitter.com/Naoki89372444" target="_blank">
            <XIcon />
        </a>
    </div>
</div>

<style>
    .container{
        display: flex;
        width: 100%;
        height: 15%;
        flex-shrink: 0;
        position: fixed;
        background-color: #1E1E1E;
    }
    .current_title{
        display: flex;
        width: 50%;
        height: 100%;
        padding: 0 2rem;
        align-items: center;
        flex-shrink: 0;
    }
    .current_title span{
        color: #D9D9D9;
        font-family: Inter;
        font-size: 5rem;
        font-style: normal;
        font-weight: 400;
        line-height: normal;
    }
    .contact{
        display: inline-flex;
        padding: 0 2rem;
        align-items: center;
        margin-left: auto;
        gap: 0 1.2rem;
    }
    .icon{
        opacity: 0.3;
    }
    .icon:hover{
        cursor: pointer;
        opacity: 1;
    }
</style>