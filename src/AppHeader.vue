<script>
export default {
    name: "AppHeader",
    data() {
        return {
            pages: [
                {
                    text: 'Characters',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Comics',
                    url: '#',
                    current: true,
                },
                {
                    text: 'Movies',
                    url: '#',
                    current: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Games',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Collectibles',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Videos',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Fans',
                    url: '#',
                    current: false,
                },
                {
                    text: 'News',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop',
                    url: '#',
                    current: false,
                },
            ]
        }
    }
}

</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col-left">

                <img src="../public/img/dc-logo.png" alt="">

            </div>
            <div class="col-right">
                <ul>
                    <li v-for="page in pages " :class="page.current"><a :href="page.url"></a>{{ page.text }}</li>
                </ul>
            </div>
        </div>
        <div class="jumbo">
            <a href="#">
                <h3>-->Content goes here </h3>
            </a>
        </div>
    </div>

</template>

<style>
* {
    box-sizing: border-box;
}

img {

    max-width: 100%;
    padding: 5px;

}

.container {
    max-width: 1048;
}

.col-left {
    width: 40%;
    display: flex;
    justify-content: left;
    align-items: center;
    vertical-align: middle;
    line-height: 150px;
}

.col-right {
    width: 60%;

}

.col-right ul {
    display: flex;
    justify-content: center;
    align-items: center;
    list-style-type: none;
    cursor: pointer;
    gap: 10px;
}

.row {
    display: flex;
    justify-content: center;
    align-items: center;

}

.jumbo {
    display: flex;
    justify-content: left;
    align-items: center;
    height: 100px;

}

.jumbo a {
    color: #fff;
    text-decoration: none;
}
</style>