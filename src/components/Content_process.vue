<template>
    <div class="section" id="porcess">
        <h3>{{ title }}</h3>
        <div class="section-box">
            <div>
                <ul>
                    <li v-for="(item, index) of list" :key="index">
                        <span>{{ list[index].date }}</span>
                        <p>{{ list[index].project }}</p>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            title: '罷免程序',
            list: [
                {
                    date: '2021.7.16',
                    project: '發布改定投票日期公告',
                },
                {
                    date: '2021.8.8',
                    project: '投票人名冊編造完成',
                },
                {
                    date: '2021.9.13',
                    project: '公告投票所設置地點',
                },
                {
                    date: '2021.10.13至10.22',
                    project: '辦理公辦電視罷免說明會',
                },
                {
                    date: '2021.10.19前',
                    project: '公告罷免投票人人數',
                },
                {
                    date: '2021.10.23',
                    project: '投票、開票',
                },
                {
                    date: '2021.10.29前',
                    project: '審定罷免投票結果',
                },
                {
                    date: '2021.10.29',
                    project: '公告罷免投票結果',
                },
            ],
        }
    },
}
</script>

<style scoped>
.section-box div {
    padding: 1rem;
    text-align: center;
}

ul {
    display: inline-block;
    max-width: 390px;
    width: 100%;
}

ul li {
    width: 100%;
    margin-bottom: 2rem;
    text-align: center;
    padding: 1rem;
    position: relative;
    background-color: #ededed;
    border-radius: 10px;
}

ul li::after {
    content: '|';
    position: absolute;
    bottom: -25px;
}

ul li:nth-last-child(1)::after {
    content: '';
}

ul li span {
    display: inline-flex;
    text-align: center;
    margin: 0 0.3rem;
    display: block;
}

ul li p {
    text-align: center;
    margin: 0;
}
</style>
