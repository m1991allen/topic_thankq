<template>
    <div class="section" id="factions">
        <h3>{{ title }}</h3>
        <div class="section-box flex">
            <div class="part1">
                <h4>反對罷免</h4>
                <div v-for="(person, index) of talk_a" :key="index">
                    <figure class="flex">
                        <img :src="person.img" :alt="person.name" />
                        <figcaption>{{ person.name }}</figcaption>
                    </figure>
                    <div class="speech">
                        <span></span>
                        <p>{{ person.speech }}</p>
                    </div>
                </div>
            </div>

            <div class="part2">
                <h4>贊成罷免</h4>
                <div v-for="(person, index) of talk_b" :key="index">
                    <figure class="flex">
                        <img :src="person.img" :alt="person.name" />
                        <figcaption>{{ person.name }}</figcaption>
                    </figure>
                    <div class="speech">
                        <span></span>
                        <p>{{ person.speech }}</p>
                    </div>
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
            // 反對
            talk_a: [
                {
                    name: '民進黨主席 蔡英文',
                    speech: `全國都很關注這次罷免案，請大家繼續關注這件事情，不要讓認真做事的人孤單，台灣的民主深化，應該是基於理性溝通，不是惡意報復。`,
                    img: require('../assets/talk_a_pre.png'),
                },
                {
                    name: '前台中市長 林佳龍',
                    speech: `罷免不應是選舉的延長戰，惡意罷免對於鼓勵年輕人投入政治、服務地方，其實是一個打擊，更可能是扼殺。`,
                    img: require('../assets/talk_a_linj.png'),
                },
                {
                    name: '民進黨立委 蔡其昌',
                    speech: `我們是立法委員，在國會審預算、修法開會是重要職責，所以時常必須在中央開會、地方服務之間找出最佳的平衡點。柏惟是我看過政治新手中，少見令人感動的年輕人，或許他沒有龐大的地方組織支撐，但他的努力，相信沒有違背投給他一票一票的海線鄉親。`,
                    img: require('../assets/talk_a_tsai.png'),
                },
                {
                    name: '民進黨立委 莊競程',
                    speech: `問政優秀、站在第一線守護台灣、為地方認真打拚的好立委，為什麼要被罷免？呼籲大家站出來力挺3Q，向罷免案說NO。`,
                    img: require('../assets/talk_a_chuang.png'),
                },
                {
                    name: '無黨籍立委 林昶佐',
                    speech: `柏惟不只是堅守台灣的國家利益，更是認真專業的立委。在國會無論出席率、質詢率都是百分百，在選區為鄉親打造最有效率的服務團隊。拜託烏日、沙鹿、龍井、大肚、烏日、霧峰的鄉親們，10月23日一定要站出來，投下反對罷免一票。挺3Q反惡霸，守護台灣民主的未來！`,
                    img: require('../assets/talk_a_lin.png'),
                },
                {
                    name: '日本神戶市議員 上畠寬弘',
                    speech: `我反對立法委員陳柏惟的罷免活動。明顯的表示，這是中國國民黨的惡質策略，要罷免陳柏惟委員，就是有利於中國共產黨及中國國民黨而已！要破壞台灣的自由、民主主義的行為，我是堅決反對，我堅定支持陳柏惟委員，希望不要被假新聞蒙蔽上當！`,
                    img: require('../assets/talk_a_jp.png'),
                },
            ],
            // 贊成
            talk_b: [
                {
                    name: '陳柏惟罷免案提議領銜人 楊文元',
                    speech: `陳柏惟就任以來，原本期待新人新氣象，最後只換來缺水、缺電、缺疫苗，和一座未來可能成為全球最大的火力發電廠。`,
                    img: require('../assets/talk_b_yang.png'),
                },
                {
                    name: '前國民黨立委 顏寬恒',
                    speech: `柏惟兄，很遺憾一切走到這裡，但您讓鄉親失了面子，少了照顧，缺了榮譽，我們別無選擇。`,
                    img: require('../assets/talk_b_yen.png'),
                },
                {
                    name: '國民黨主席 朱立倫',
                    speech: `陳柏惟在國會評鑑拿到「0顆星」、「0提案」、「0通過」，還不關心台中用肺發電問題、主張大麻合法化，這就是民進黨蔡英文主席口中的好立委嗎？`,
                    img: require('../assets/talk_b_jui.png'),
                },
                {
                    name: '中國廣播公司董事長 趙少康',
                    speech: `請海線鄉親一定要站出來，罷免這個污染下一代視聽，只會苦行作秀、肇事逃逸、阻擋疫苗、支持萊豬、分裂族群以謀取政治利益的政客，還給海線一個清新、團結的未來！`,
                    img: require('../assets/talk_b_chao.png'),
                },
            ],
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
