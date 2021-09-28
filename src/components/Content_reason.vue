<template>
    <div class="section" id="reason">
        <h3>{{ title }}</h3>
        <div class="section-box">
            <p>{{ descript }}</p>
            <ul>
                <li v-for="(item, index) of list" :key="index">
                    {{ list[index].title }}
                    <p>
                        {{ list[index].content }}
                    </p>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            title: '罷免理由',
            descript: '提議人之領銜人楊文元先生提出之罷免理由書如下：',
            list: [
                {
                    title: '（一）無心地方服務，承諾政見一再跳票：',
                    content: '針對台中火力發電廠、台中空氣品質、於台灣各地廣設服務處等議題',
                },
                {
                    title: '（二）無心監督民意所託，背離選區民意：',
                    content: '針對萊克多巴胺美國豬肉進口、大麻、社會犯罪等議題',
                },
                {
                    title: '（三）發言荒腔走板，失格、失言新聞頻傳：',
                    content: '針對立法院質詢、臉書發文',
                },
                {
                    title: '（四）面對反對聲音，經常使用暴力及恐嚇言論：',
                    content: '針對追打立委吳怡玎、揚言提告民眾等事件',
                },
            ],
        }
    },
}
</script>

<style scoped>
.section-box {
    max-width: 420px;
}
</style>
