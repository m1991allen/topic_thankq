<template>
    <div class="section" id="profile">
        <h3>{{ title }}</h3>
        <div class="section-box">
            <div class="flex">
                <figure>
                    <img src="../assets/profile.jpg" alt="陳柏惟" />
                    <figcaption class="name">{{ name }}</figcaption>
                </figure>
                <article>
                    <p style="margin-left: 1rem; margin-bottom:0">學歷：</p>
                    <ul>
                        <li style="margin-bottom: 2rem;">{{ detail.edu }}</li>
                    </ul>
                    <p style="margin-left: 1rem; margin-bottom:0">經歷：</p>
                    <ul>
                        <li v-for="(item, index) of detail.exp" :key="index">{{ detail.exp[index] }}</li>
                    </ul>
                </article>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            title: '被罷免人背景',
            name: '陳柏惟',
            detail: {
                edu: '國立高雄大學資訊管理學系學士',
                exp: ['台灣基進發言人', '第10屆立法委員'],
            },
        }
    },
}
</script>

<style scoped>
.flex {
    justify-content: center;
}

.flex img {
    max-width: 200px;
}

@media screen and (max-width: 768px) {
    .flex img {
        max-width: 150px;
    }
}

p {
    text-align: left;
    font-size: 1.2rem;
}

ul li {
    font-size: 1.2rem;
    margin: 1rem 0 1rem 2rem;
}

@media screen and (max-width: 768px) {
    p,
    ul li {
        font-size: 1rem;
    }
}
</style>
