<template>
    <div class="section" id="factions">
        <h3>{{ title }}</h3>
        <div class="section-box flex">
            <div class="part1">
                <h4>反對罷免</h4>
                <figure class="flex">
                    <img src="../assets/dis_tsai.png" alt="民進黨立委 蔡其昌" />
                    <figcaption>{{ talk.person1.name }}</figcaption>
                </figure>
                <div class="speech">
                    <span></span>
                    <p>{{ talk.person1.speech }}</p>
                </div>

                <figure class="flex">
                    <img src="../assets/dis_chuang.png" alt="民進黨立委 莊競程" />
                    <figcaption>{{ talk.person2.name }}</figcaption>
                </figure>
                <div class="speech">
                    <span></span>
                    <p>{{ talk.person2.speech }}</p>
                </div>
            </div>
            <div class="part2">
                <h4>贊成罷免</h4>
                <figure class="flex">
                    <img src="../assets/age_yen.png" alt="民進黨立委 顏寬恒" />
                    <figcaption>{{ talk.person3.name }}</figcaption>
                </figure>
                <div class="speech">
                    <span></span>
                    <p>{{ talk.person3.speech }}</p>
                </div>

                <figure class="flex">
                    <img src="../assets/age_jui.png" alt="民進黨立委 朱立倫" />
                    <figcaption>{{ talk.person4.name }}</figcaption>
                </figure>
                <div class="speech">
                    <span></span>
                    <p>{{ talk.person4.speech }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            title: '各方說法',
            talk: {
                person1: {
                    name: '民進黨立委 蔡其昌',
                    speech: `我們是立法委員，在國會審預算、修法開會是重要職責，所以時常必須在中央開會、地方服務之間找出最佳的平衡點。柏惟是我看過政治新手中，少見令人感動的年輕人，或許他沒有龐大的地方組織支撐，但他的努力，相信沒有違背投給他一票一票的海線鄉親。`,
                },
                person2: {
                    name: '民進黨立委 莊競程',
                    speech: `問政優秀、站在第一線守護台灣、為地方認真打拚的好立委，為什麼要被罷免？呼籲大家站出來力挺3Q，向罷免案說NO。`,
                },
                person3: {
                    name: '前國民黨立委 顏寬恒',
                    speech: `柏惟兄，很遺憾一切走到這裡，但您讓鄉親失了面子，少了照顧，缺了榮譽，我們別無選擇。`,
                },
                person4: {
                    name: '國民黨主席 朱立倫',
                    speech: `陳柏惟在國會評鑑拿到「0顆星」、「0提案」、「0通過」，還不關心台中用肺發電問題、主張大麻合法化，這就是民進黨蔡英文主席口中的好立委嗎？`,
                },
            },
        }
    },
}
</script>

<style scoped>
h4 {
    text-align: right;
    font-size: 1.2rem;
    font-weight: 900;
    background-color: rgb(158, 158, 158);
    padding: 10px;
    color: white;
    border-radius: 0 10px 0px 0;
}

.flex {
    align-items: flex-end;
}

figure {
    text-align: left;
    margin-top: 2rem;
}
figure img {
    max-width: 100px;
    text-align: left;
}
figure figcaption {
    font-size: 1.2rem;
    margin: 0 0 1rem 1rem;
}

.speech p {
    text-align: left;
    line-height: 1.8rem;
    background-color: #ffffff;
    padding: 1rem;
    margin: 0;
    border-radius: 10px;
}

.speech span {
    display: block;
    width: 0;
    height: 0;
    border-style: solid;
    border-width: 30px 0 0 30px;
    border-color: transparent transparent transparent #ffffff;
    transform: translateX(60px);
}

.section-box {
    max-width: 500px;
}

.section-box .part1 {
    background-color: #ededed;
    padding: 1rem;
    border-radius: 10px;
    margin-bottom: 2rem;
}

.section-box .part2 {
    background-color: #ededed;
    padding: 1rem;
    border-radius: 10px;
    margin-top: 2rem;
}

#factions .flex {
    display: flex;
    align-items: baseline;
    max-width: 100%;
}

.part1,
.part2 {
    width: 50%;
    margin: 1rem;
}

@media screen and (max-width: 768px) {
    #factions .flex {
        display: block !important;
    }

    .part1,
    .part2 {
        width: 100%;
        margin: 0px;
    }
}
</style>
