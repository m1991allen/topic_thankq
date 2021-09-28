<template>
    <div>
        <p>{{ date }}</p>
        <div class="outside">
            <div class="inner">
                <h2><span>陳柏惟</span><span>罷免案</span></h2>
                <p>開票、門檻一次看！</p>
                <a href="#voting">點我看開票</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            date: '2021/10/23',
        }
    },
}
</script>

<style scoped>
h2 {
    margin: 2rem;
    font-weight: bolder;
}

.outside {
    background-color: #a73f24;
    width: 100%;
    height: 450px;
    transform: rotate(-2deg);
    overflow-x: hidden;
}

.inner {
    background-color: #fff;
    width: 105%;
    height: 400px;
    position: absolute;
    transform: translate(-2%, 6%) rotate(-1deg);
}

h2 span {
    display: block;
    color: black;
    font-size: 4rem;
    margin: 1rem 0;
}

/* 文字：陳柏惟罷免案 */

h2 span:nth-child(1) {
    transform: translateX(-3%);
    animation: rightToLeft 2s;
}

h2 span:nth-child(2) {
    transform: translateX(3%);
    animation: leftToRight 2s 0.5s forwards;
    opacity: 0;
}

/* 文字：開票門檻一次看 */
.inner p {
    color: #a73f24;
    font-size: 2rem;
    padding: 0.5rem;
    text-align: left;
    border: 3px solid #a73f24;
    display: inline-block;
    transform: translateX(0px);
    line-height: 3rem;
    white-space: nowrap;
}

@keyframes rightToLeft {
    0% {
        transform: translateX(0%);
        opacity: 0;
    }
    100% {
        transform: translateX(-3%);
        opacity: 1;
    }
}

@keyframes leftToRight {
    0% {
        transform: translateX(0%);
        opacity: 0;
    }
    100% {
        transform: translateX(3%);
        opacity: 1;
    }
}

p {
    transform: translateY(-3px) rotate(-2deg);
    font-size: 3rem;
    margin: 0 1rem;
    color: #a73f24;
    text-align: left;
    font-weight: bolder;
}

a {
    display: block;
    background-color: #384776;
    color: white;
    font-size: 1.4rem;
    max-width: 200px;
    margin: 2rem auto;
    padding: 0.5rem;
}
</style>
