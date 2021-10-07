<template>
    <div class="section" id="voting">
        <h3>{{ title }}</h3>
        <div class="section-box">
            <div class="iframe-container">
                <iframe
                    src="https://www.youtube.com/embed/XxJKnDLYZz4"
                    title="YouTube video player"
                    frameborder="0"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen
                ></iframe>
            </div>
            <div class="vote">
                <!-- 同意票 -->
                <div class="votebox"><span id="agree_bar"></span></div>
                <p>{{ title_agree }}<span id="agree_vote"></span></p>

                <!-- 不同意票 -->
                <div class="votebox"><span id="disagree_bar"></span></div>
                <p>{{ title_disagree }}<span id="disagree_vote"></span></p>

                <!-- 開票結果 -->
                <p style="text-align:center;">開票結果：開票中</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            title: '開票直播',
            title_agree: '同意（門檻：72,781）: ',
            title_disagree: '不同意： ',
            vote_ag: '7500',
            vote_dag: '75000',
            vote_tatol: 150000,

            vote:{
                agree: 123, //同意票
                disagree: 123, //不同意票
            }
        }
    },

    methods: {
        voting() {
            let vote_agree = this.vote_ag
            let vote_disagree = this.vote_dag

            let bar_agree = Math.floor((this.vote_ag / this.vote_tatol) * 100)
            let bar_disagree = Math.floor((this.vote_dag / this.vote_tatol) * 100)

            document.getElementById('agree_vote').innerText = vote_agree.replace(/\B(?=(\d{4})+(?!\d))/g, '萬')
            document.getElementById('disagree_vote').innerText = vote_disagree.replace(/\B(?=(\d{4})+(?!\d))/g, '萬')

            document.getElementById('agree_bar').style.width = bar_agree + '%'
            document.getElementById('disagree_bar').style.width = bar_disagree + '%'
        },
    },

    mounted() {
        this.voting()
    },
}
</script>

<style scoped>
.iframe-container {
    overflow: hidden;
    padding-top: 56.25%;
    position: relative;
}
.iframe-container iframe {
    border: 0;
    height: 100%;
    left: 0;
    position: absolute;
    top: 0;
    width: 100%;
}

/* 4x3 縱橫比 */
.iframe-container-4x3 {
    padding-top: 75%;
}

.vote {
    margin: 2rem 0;
}

.votebox {
    background-color: #aaaaaa;
    width: 100%;
    height: 30px;
    border-radius: 10px;
    display: flex;
}

.votebox span {
    border-radius: 10px;
}

/* 票數據條 */
#agree_bar {
    width: 30%;
    background-color: #374574;
}

#disagree_bar {
    width: 30%;
    background-color: #743737;
}
</style>
