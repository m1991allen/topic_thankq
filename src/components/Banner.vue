<template>
    <div class="main">
        <h1>{{ title }}</h1>
        <p>{{ date }}</p>
        <h2>{{ subtitle }}</h2>
        <a class="click-me" href="#voting">點我 <i class="far fa-mouse-pointer"></i></a>
    </div>
    <div class="main-mb">
        <img src="../assets/main_bg_mb.svg" />
        <a class="click-me" href="#voting">點我 <i class="far fa-mouse-pointer"></i></a>
    </div>
</template>

<script>
export default {
    data() {
        return {
            title: '陳柏惟罷免案',
            date: '10/23',
            subtitle: '開票、門檻一次看',
        }
    },
}
</script>

<style scoped>
@font-face {
    font-family: DFT_B9;
    src: url(https://www.ftvnews.com.tw/topics/thankq/font/DFT_B9.ttf);
}

.main {
    font-family: DFT_B9, Helvetica, Arial, sans-serif, 微軟正黑體, 蘋果儷中黑;
    font-weight: lighter;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    background-image: url(../assets/main_bg.png);
    background-position: center center;
    background-repeat: no-repeat;
    background-size: cover;
    min-width: 100%;
    max-width: 2000px;
    height: 1000px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}

.click-me {
    font-size: 1.4rem;
    background-color: #fff;
    padding: 0.5rem 1rem;
    outline: rgb(255, 252, 49) 1px solid;
    animation: outline 1s linear infinite;
}

/* 背景桌機版設定 */
.main .click-me {
    transform: translateY(100%);
}

/* 背景手機版設定 */
.main-mb {
    display: none;
    position: relative;
}

.main-mb .click-me {
    position: absolute;
    top: 65%;
    left: 50%;
    transform: translateX(-50%);
    font-size: 1rem;
}

@keyframes outline {
    0% {
        outline: rgb(255, 252, 49) 1px solid;
    }
    100% {
        outline: rgba(255, 255, 255, 0) 10px solid;
    }
}

img {
    width: 100%;
}

@media screen and (max-width: 768px) {
    .main {
        display: none;
    }
    .main-mb {
        display: block;
    }
}

.main h1 {
    font-size: 5rem;
    color: white;
}

.main h2 {
    font-size: 3rem;
    color: white;
}

.main p {
    font-size: 2rem;
    padding-top: 2rem;
    color: white;
    text-align: center;
}

h1,
h2,
p {
    text-shadow: 3px 3px 10px black;
}
</style>
