<script>
    let isLifting = false;
    export let card_title = '';
    export let path = '';
    const toggleLift = () =>{
        isLifting = isLifting ? false : true;
    }
</script>

<div class='card {isLifting ? 'bouncing' : ''}' on:mouseover={toggleLift} on:mouseout={toggleLift}>
    <a href="{path}" />
    <p>
        {card_title}
    </p>
</div>

<svelte:head>
  <link href='https://fonts.googleapis.com/css?family=Noto+Sans+JP' rel='stylesheet'>
</svelte:head>

<style>
    .card{
        display: flex;
        position: relative;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        width: 11rem;
        height: 8rem;
        background-color: #453fa9;
        box-shadow: 0rem 1rem 0.8rem rgb(0, 0, 0);
        border-radius: 1rem;
        transition: opacity 0.2s ease-in-out;
    }
    .card:hover{
        cursor: pointer;
    }
    .card.bouncing{
        opacity: 0.7;
    }
    .card p{
        font-family: Noto Sans JP;
        font-size: 2rem; 
        font-weight: bold;
        color: #eeeeee;
    }
    .card a{
        position: absolute;
        width: 100%;
        height: 100%;
    }
</style>
