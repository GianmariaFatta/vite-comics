<script>
import CreateJumbo from './CreateJumbo.vue';
export default {
    name: "AppHeader",
    data() {
        return {
            currentIndex: 1,
            pages: [
                {
                    text: 'CHARACTERS',
                    url: '#',
                    current: false,
                },
                {
                    text: 'COMICS',
                    url: '#',
                    current: true,
                },
                {
                    text: 'MOVIES',
                    url: '#',
                    current: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false,
                },
                {
                    text: 'GAMES',
                    url: '#',
                    current: false,
                },
                {
                    text: 'COLLECTIBLES',
                    url: '#',
                    current: false,
                },
                {
                    text: 'VIDEOS',
                    url: '#',
                    current: false,
                },
                {
                    text: 'FANS',
                    url: '#',
                    current: false,
                },
                {
                    text: 'NEWS',
                    url: '#',
                    current: false,
                },
                {
                    text: 'SHOP',
                    url: '#',
                    current: false,
                },
            ]
        }
    }, methods: {
        setCurrentIndex(index) {
            this.currentIndex = index
        }
    }, components: { CreateJumbo }
}

</script>

<template>
    <header>
        <div class="container">
            <div class="row">
                <div class="col-left">
                    <div class="card">
                        <a href=""><img src="../assets/img/dc-logo.png" alt=""></a>
                    </div>
                </div>
                <div class="col-right">
                    <ul>
                        <li v-for="(page, i) in pages " :class="{ 'active': i === currentIndex }"
                            @click="setCurrentIndex(i)"><a :href="page.url" :key="page.text"></a>{{ page.text }}
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
    <CreateJumbo />

</template>

<style scoped lang="scss">
@use '../assets/scss/mixins' as*;

header {
    background-color: #fff;
    width: 100%;
    height: 100px;
}

.col-left {
    @include left_flex;
    width: 40%;
    // border: 2px dashed darkblue
}

.col-right {
    width: 60%;
    height: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    // border: 2px dashed darkred;

    ul {
        @include center-flex;
        list-style-type: none;
        cursor: pointer;
        gap: 30px;
    }
}


.row {
    @include center-flex;
    width: 100%;
}

.card {
    @include center-flex;
    width: 80px;
    margin: 10px;
}

.active {
    color: dodgerblue;
    border-bottom: 5px solid dodgerblue;
}

li {
    padding: 33px 3px;
    font-size: 18px;
    font-weight: bold;
}
</style>