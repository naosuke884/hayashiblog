<script>
    import Head from "./Head.svelte";
    import Top from  "./Top.svelte";
    import About from "./About.svelte";
    import Log from "./Log.svelte";

    let titles = {
        "top": "",
        "about": "About",
        "log": "Log",
        "works": "Works",
    };
    let title_key = "top";
    let title = titles[title_key];
    const changeTitle = (event) => {
        title_key = event.detail.title_key;
        title = titles[title_key];
    };
</script>

<div class='container'>
    <Head bind:title />
    <Top bind:title_key on:changeTitle={changeTitle} />
    <About bind:title_key on:changeTitle={changeTitle} />
    <Log bind:title_key on:changeTitle={changeTitle} />
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
