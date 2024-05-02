<script>
    import Head from '$lib/Head.svelte';
</script>

<div class='container'>
    <div class='head'>
        <Head />
    </div>
    <div class='wrapper'>
        <slot></slot>
    </div>
</div>

<style>
    .container{
        width: 100%;
        height: 100%;
    }
    .head{
        width: 100%;
        height: 15%;
    }
    .wrapper{
        width: 100%;
        height: 85%;
    }
</style>
