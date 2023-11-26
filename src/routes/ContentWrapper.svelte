<script>
    import { createEventDispatcher } from 'svelte';
    import { onMount } from 'svelte';
    const dispatch = createEventDispatcher();
    let el;
    let rect;
    export let title_key;
    export let current_title_key;
    const changeTitleDispatch = ()=>{
        if (current_title_key != title_key && rect.bottom - window.scrollY <= window.innerHeight){
            dispatch('changeTitle', { 'title_key': title_key});
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
    <slot>
        Hi…('_')/
    </slot>
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