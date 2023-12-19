<script>
    import { createEventDispatcher } from 'svelte';
    import { onMount } from 'svelte';
    const dispatch = createEventDispatcher();
    let element;
    export let title_key;
    const changeTitleDispatch = ()=>{
        dispatch('changeTitle', { 'title_key': title_key});
    };
    onMount(() => {
        let rect = element.getBoundingClientRect();
        const top = rect.top - rect.top / 4;
        const bottom = rect.bottom;
        window.addEventListener('scroll', () => {
            if (top <= window.scrollY && window.scrollY < bottom){
                changeTitleDispatch();
            }
        });
    });
</script>

<div class='container' bind:this={element}>
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