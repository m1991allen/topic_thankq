<template>
    <div class="section" id="recall">
        <h3>{{ title }}</h3>
        <div class="section-box">
            <p>{{ content }}</p>
            <ul>
                <li v-for="item in list" :key="item.id">
                    {{ item }}
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            title: '罷免門檻',
            content: `依照《公職人員選舉罷免法》第九十條第一項，罷免投票的通過門檻必須同時符合以下兩條件：`,
            list: [
                `（一）有效同意票數多於不同意票。`,
                `（二）同意票數達原選舉區選舉人總數四分之一以上。`,
                `因此以台中選委會公布本次罷免案投票人人數「29萬4976人」來算，罷免同意票門檻為「7萬3744人」、同意罷免票需多於不同意票數。`,
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
