<script>
export default {
    name: "AppHeader",
    data() {
        return {
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
    }
}

</script>

<template>
    <header>
        <div class="container">
            <div class="row">
                <div class="col-left">
                    <div class="card">
                        <img src="../assets/img/dc-logo.png" alt="">
                    </div>
                </div>
                <div class="col-right">
                    <ul>
                        <li v-for="page in pages " class=""><a :href="page.url" :key="page.text"></a>{{ page.text }}
                        </li>
                    </ul>
                </div>
            </div>

            <!-- <div class="jumbo">
            <div class="row">

                <a href="#">
                    <h3>Content goes here</h3>
                </a>
            </div>
        </div> -->
        </div>
    </header>
</template>

<style scoped lang="scss">
@use '../assets/scss/mixin' as*;



header {
    background-color: #fff;
    width: 100%;
    height: 95px;
}

.col-left {
    width: 40%;
    display: flex;
    justify-content: left;
    align-items: center;
}

.col-right {
    width: 60%;
    height: auto;
    display: flex;
    justify-content: left;
    align-items: center;

}

.col-right ul {
    @include center-flex;
    list-style-type: none;
    cursor: pointer;
    gap: 10px;
}

.row {
    width: 100%;
    @include center-flex;

}

.jumbo {
    display: flex;
    justify-content: left;
    align-items: left;
    height: 100px;
    width: 100%;
    border: 2px solid red;

}

.jumbo a {
    color: #fff;
    text-align: left;
}

.card {
    @include center-flex;
    width: 80px;
    margin: 10px;
}

.active {
    color: dodgerblue;
    border-bottom: 4px solid dodgerblue;
}

li {
    padding: 32px 0;
    font-size: 13px;
    font-weight: bold;
}
</style>