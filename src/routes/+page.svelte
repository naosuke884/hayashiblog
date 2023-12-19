<script>
    import Head from "./Head.svelte";
    import Top from  "./ContentTop.svelte";
    import About from "./ContentAbout.svelte";
    import Log from "./ContentLog.svelte";
    import ContentWrapper from "./ContentWrapper.svelte";
    import { onMount } from 'svelte';

    let titles = {
        "top": "",
        "about": "About",
        "log": "Log",
        "works": "Works",
    };
    let contents = [
        {'title_key': 'top', 'component': Top},
        {'title_key': 'about', 'component': About},
        {'title_key': 'log', 'component': Log},
    ];
    let current_title_key = "top";
    let current_title = titles[current_title_key];
    const changeTitle = (event) => {
        current_title_key = event.detail.title_key;
        current_title = titles[current_title_key];
    };
</script>

<div class='container'>
    <Head bind:current_title />
    {#each contents as content}
        <ContentWrapper
            title_key={content.title_key}
            on:changeTitle={changeTitle}
        >
            <svelte:component this={content.component} />
        </ContentWrapper>
    {/each}
</div>

<style>
    .container{
        display: flex;
        flex-direction: column;
        width: 100%;
        height: 100%;
        flex-shrink: 0;
    }
</style>
