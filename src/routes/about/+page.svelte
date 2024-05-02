<script>
    import LogRow from './LogRow.svelte';
</script>

<div class='container'>
    <div class='profiel'>
        <img src='bird.png' alt=''>
        <div class='brief'>
            <p class='name'>Hayashi Naoki</p>
            <p>愛知工業大学に所属しています<br>プログラミングと機会学習を学んでいます</p>
        </div>
    </div>
    <div class='log'>
        <div class='log_title'>
            <p>Log</p>
        </div>
        <div class='log_content'>
            <LogRow date='2024/04' content='愛知工業大学院の経営情報科学研究科に入学' />
            <LogRow date='2024/03' content='愛知工業大学を卒業' />
            <LogRow date='2020/04' content='愛知工業大学の情報科学部に入学' />
        </div>
    </div>
</div>

<style>
    .container{
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }
    .profiel{
        width: 50%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 2rem;
    }
    .profiel img{
        width: 10rem;
        height: 10rem;
        border-radius: 50%;
        border: 0.3rem solid #3c3b48;
        box-shadow: 0rem 0rem 4rem rgb(0, 0, 0);
    }
    .brief{
        width: 80%;
        color: #eeeeee;
        border-left: 0.1rem solid #3c3b48;
        padding-left: 1rem;
        font-size: 1rem;
    }
    .name{
        font-size: 2rem;
        font-weight: bold;
        margin-bottom: 1rem;
        margin-top: 0;
    }
    .log{
        width: 50%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: start;
        flex-direction: column;
    }
    .log_title{
        width: 100%;
        height: 100%;
        color: #eeeeee;
        font: 3rem Noto Sans JP;
        font-weight: bold;
    }
    .log_content{
        width: 80%;
        height: 100%;
    }
</style>
