<template>
    <div class="bottom">
        <a href="#voting"><i class="fad fa-vote-nay"></i> 即時開票</a>
        <a href="#recall"><i class="fad fa-chart-pie"></i> 罷免門檻</a>
        <a href="#news"><i class="fad fa-rss"></i> 相關新聞</a>
    </div>
</template>

<script>
export default {}
</script>

<style>
.bottom {
    display: flex;
    position: fixed;
    bottom: 0;
    width: 100%;
    background-color: #374674;
    z-index: 999;
}
.bottom a {
    width: 33.3%;
    padding: 1rem;
    color: white;
}
</style>
