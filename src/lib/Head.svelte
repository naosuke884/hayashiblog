<script>
    import GithubIcon from './HeadGithubIcon.svelte';
    import XIcon from './HeadXIcon.svelte';
    import HomeButton from './HeadHomeButton.svelte';

    const to_github = 'https://github.com/naosuke884'
    const to_x = 'https://twitter.com/Naoki89372444'
</script>

<div class='container'>
    <div class='to_home'>
        <HomeButton />
    </div>
    
    <div class='contact'>
        <a class='icon github-icon' href={to_github} target='_blank'>
            <GithubIcon />
        </a>
        <a class='icon x-icon' href={to_x} target='_blank'>
            <XIcon />
        </a>
    </div>
</div>

<style>
    .container{
        display: flex;
        width: 100%;
        height: 100%;
        flex-shrink: 0;
        background-color: #1E1E1E;
        box-shadow: 0rem 0.8rem 1rem rgb(0, 0, 0);
        position: relative;
    }
    .to_home{
        display: inline-flex;
        padding: 0 2rem;
    }
    .contact{
        display: inline-flex;
        padding: 0 2rem;
        align-items: center;
        margin-left: auto;
        gap: 0 1.2rem;
    }
    .icon{
        transition: opacity 0.2s ease-in-out;
        opacity: 0.7;
    }
    .icon:hover{
        cursor: pointer;
        opacity: 1;
    }
</style>