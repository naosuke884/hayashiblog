<script>
    export let date = '';
    export let content = '';
</script>
<div class='container'>
    <span class='date'>
        <p>{date}</p>
    </span>
    <span class='content'>
        <p>{content}</p>
    </span>
</div>
<style>
    .container{
        display: inline-flex;
        width: 100%;
        color: #eeeeee;
        font: 1rem Noto Sans JP;
        gap: 2rem;
        border-bottom: 0.1rem solid #3c3b48;
    }
</style>