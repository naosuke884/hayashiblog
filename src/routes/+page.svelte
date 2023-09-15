<script>
    import Card from "./Card.svelte";
    const titles = ["Item 1", "Item 2", "Item 3"];
</script>

<div>
    {#each titles as title}
        <Card {title} />
    {/each}
</div>

<style>
</style>
