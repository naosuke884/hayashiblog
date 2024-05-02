<script>
    let isScaling = false;
    const toggleScale = () =>{
        isScaling = isScaling ? false : true;
    }
</script>

<div class='container'>
    <div class='circle {isScaling ? 'scaling' : ''}' on:mouseover={toggleScale} on:mouseout={toggleScale}>
        <a href="/"></a>
    </div>
</div>

<style>
    .container{
        display: flex;
        width: 100%;
        height: 100%;
        justify-content: center;
        align-items: center;
    }
    .circle{
        width: 3rem;
        height: 3rem;
        border-radius: 50%;
        background-color: #453fa9;
        box-shadow: 0rem 0rem 3rem rgb(0, 0, 0);
        transition: transform 0.2s ease-in-out, opacity 0.5s ease-out;
        display: flex;
        justify-content: center;
        align-items: center;
        position: relative;
        opacity: 0.7;
    }
    /* .circle p{
        font-family: Noto Sans JP;
        font-size: 0.7rem;
        font-weight: bold;
        color: #eeeeee;
        opacity: 0;
    }
    .circle.scaling p{
        opacity: 1;
    } */
    .circle:hover{
        cursor: pointer;
        transform: scale(1.5);
        opacity: 1;
    }
    .circle a{
        position: absolute;
        width: 100%;
        height: 100%;
    }
</style>