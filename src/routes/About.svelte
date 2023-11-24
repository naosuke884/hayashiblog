<script>
    import { createEventDispatcher } from 'svelte';
    import { onMount } from 'svelte';
    const dispatch = createEventDispatcher();
    let el;
    let rect;
    const val = "about";
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
</div>

<style>
    .container{
        display: flex;
        height: 85%;
        justify-content: center;
        align-items: center;
        flex-shrink: 0;
        background: #D9D9D9;
    }
</style>