<template>
    <div class="section" id="voted">
        <h3>{{ title }}</h3>
        <div class="section-box">
            <div class="flex">
                <figure>
                    <img src="../assets/cha_chen.png" alt="陳柏惟" />
                </figure>
                <p class="name">陳柏惟 <span>vs</span> 顏寬恒</p>
                <figure>
                    <img src="../assets/cha_yen.png" alt="陳柏惟" />
                </figure>
            </div>
            <div>
                <img class="votebar" src="../assets/votebar.png" alt="票數" />
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            title: '2020台中第二選區結果',
        }
    },
}
</script>

<style scoped>
figure img {
    max-width: 100px;
}

.votebar {
    max-width: 600px;
    width: 100%;
    margin: 1rem 0;
}

.flex {
    justify-content: space-around;
    align-items: center;
}
.flex p {
    position: relative;
}
.flex p::before {
    content: '勝';
    background-color: #c1272d;
    color: white;
    padding: 0.5rem;
    position: absolute;
    top: -35px;
    left: -40px;
    border-radius: 100%;
    transform: rotate(-15deg);
}

@media screen and (max-width: 500px) {
    span {
        display: block;
    }
}

@media screen and (max-width: 350px) {
    .flex p::before {
        left: 40px;
    }
}
</style>
