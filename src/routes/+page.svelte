<script>
    import Card from '$lib/Card.svelte';

    const cards = [
        {path: '/about', title: 'About'},
        {path: '/works', title: 'Works'},
    ];
</script>

<div class='container'>
    <div class='wrapper'>
        <div class='title'>
            <p>Hayashi Naoki's Portfolio</p>
        </div>
        <div class='cards'>
            {#each cards as card}
                <Card card_title={card.title} path={card.path} />
            {/each}
        </div>
    </div>
</div>

<style>
    .container{
        width: 100%;
        height: 85%;
        color: #eeeeee;
        font: 2rem Noto Sans JP;
    }
    .wrapper{
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .title{
        width: 100%;
        height: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        opacity: 0.7;
        background-color: #27237b;
    }
    .cards{
        width: 100%;
        height: 50%;
        display: flex;
        flex-wrap: wrap;
        gap: 5rem;
        justify-content: center;
        align-items: center;
    }
</style>
