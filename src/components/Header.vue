<template>
    <div class="progress"></div>
    <div class="flex-logo">
        <i class="fad fa-2x fa-list" @click="menu">
            <nav class="nav">
                <a v-for="(item, index) of list" :key="index" :href="item.anchor">
                    <i class="fad fa-scrubber"></i> {{ item.title }}
                </a>
            </nav>
        </i>

        <figure>
            <img class="logo" src="../assets/logo_ftvn.png" alt="民視新聞網" />
        </figure>
    </div>
</template>

<script>
export default {
    data() {
        return {
            list: [
                {
                    title: '新聞直播',
                    anchor: '#voting',
                },
                {
                    title: '被罷免人背景',
                    anchor: '#profile',
                },
                {
                    title: '2020選舉結果',
                    anchor: '#voted',
                },
                {
                    title: '罷免理由',
                    anchor: '#reason',
                },
                {
                    title: '罷免程序',
                    anchor: '#porcess',
                },
                {
                    title: '罷免門檻',
                    anchor: '#recall',
                },
                {
                    title: '各方說法',
                    anchor: '#factions',
                },
                {
                    title: '相關新聞',
                    anchor: '#news',
                },
            ],
        }
    },
    methods: {
        scroll() {
            window.addEventListener('scroll', () => {
                this.moveBar('#374674')
            })
        },

        moveBar(color = '#0984e3') {
            let bar = document.querySelector('.progress')
            let w = Math.ceil(
                (Math.round(window.pageYOffset) / (document.body.scrollHeight - window.innerHeight)) * 100
            )
            bar.style.width = w + '%'
            bar.style.background = color
        },

        menu() {},
    },
    mounted() {
        this.scroll()
        this.moveBar()
    },
}
</script>

<style scoped>
.flex-logo {
    margin: 1rem;
    margin-bottom: 3rem;
    text-align: left;
}

/* 漢堡選單 */
.fa-list {
    color: #a73f24;
    cursor: pointer;
    position: fixed;
    z-index: 999;
    right: 1rem;
    background-color: white;
    border-radius: 10px;
    padding: 5px;
    padding: 5px;
    box-shadow: 1px 2px 3px black;
}
.nav {
    width: 250px;
    padding: 1rem;
    position: fixed;
    background-color: #f67351f0;
    z-index: 998;
    top: 3.3rem;
    right: 1rem;
    border-radius: 10px;
    display: none;
}

.fa-list:hover .nav {
    display: block;
}
.nav a {
    font-size: 1rem;
    margin: 1rem;
    display: block;
    color: white;
    font-weight: bolder;
}

.logo {
    max-width: 100%;
    width: 300px;
}

@media screen and (max-width: 768px) {
    .logo {
        width: 200px;
    }
}

@media screen and (max-width: 450px) {
    .logo {
        width: 200px;
    }
}

/* 進度條 */
.progress {
    position: fixed;
    top: 1px;
    width: 0.5%;
    height: 10px;
    z-index: 999;
}
</style>
