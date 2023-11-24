<script>
    import { createEventDispatcher } from 'svelte';
    import { onMount } from 'svelte';
    const dispatch = createEventDispatcher();
    let el;
    let rect;
    const val = "top";
    export let title_key;
    const changeTitleDispatch = ()=>{
        if (title_key != val && rect.bottom - window.scrollY <= window.innerHeight){
            dispatch('changeTitle', { "title_key": val});
        };
    };
    onMount(() => {
        rect = el.getBoundingClientRect();
        changeTitleDispatch();
        window.addEventListener('scroll', () => {
            changeTitleDispatch();
        });
    });
</script>

<div class='container' bind:this={el}>
    <span class='title'>
        Naoki's Portfolio
    </span>
</div>

<style>
    .container{
        display: flex;
        height: 100%;
        justify-content: center;
        align-items: center;
        flex-shrink: 0;
    }
    .title{
        color: #D9D9D9;
        text-align: center;
        font-family: Inter;
        font-size: 8rem;
        font-style: normal;
        font-weight: 400;
        line-height: normal;
    }
</style>