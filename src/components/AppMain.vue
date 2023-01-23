<script>
import AppCard from './AppCard.vue';
export default {
    name: "AppMain",
    data() {
        return {
            comicsLinks: ["Characters", "Comics", "Movies", "TV", "Games", "Collectibles", "Videos", "Fans", "News"],
            shopLinks: ["Shop DC", "Shop Dc Collectibles"],
            dcLinks: ["Terms Of Use", "Privacy policy (new)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshop", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"],
            sitesLinks: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "Dc Power Visa"],
        }
    }, components: { AppCard },
    props: {
        comics: Array
    }
}

</script>

<template>
    <main>
        <div id="contents">
            <div class="container">
                <div class="comic-row">
                    <AppCard v-for="comic in comics" :key="comic.series" :comic="comic" />
                </div>
            </div>
            <div class="row-button">
                <button><a href=""> LOAD MORE</a></button>
            </div>
        </div>
        <section>
            <ul>
                <li><a href="">DIGITAL COMICS</a> </li>
                <li><a href="">DC MERCHANDISE</a> </li>
                <li><a href="">SUBSCRIPTION</a> </li>
                <li><a href="">COMIC SHOP LOCATOR</a> </li>
                <li><a href="">DC POWER VISA</a> </li>
            </ul>
        </section>
        <div id="comics">
            <div class="container">
                <div class="row">
                    <div class="col-left">
                        <div class="s-column">
                            <h3>DC COMICS</h3>
                            <ul>
                                <li v-for="comicsLink in comicsLinks"> <a href=""> {{ comicsLink }}</a></li>
                            </ul>
                            <h3>SHOP</h3>
                            <ul>
                                <li v-for="shopLink in shopLinks"><a href="">{{ shopLink }}</a></li>

                            </ul>
                        </div>
                        <div class="m-column">
                            <h3>DC </h3>
                            <ul>
                                <li v-for="dcLink in dcLinks"><a href="">{{ dcLink }} </a></li>

                            </ul>
                        </div>
                        <div class="e-column">
                            <h3>SITES</h3>
                            <ul>
                                <li v-for="siteLink in sitesLinks"> <a href=""> {{ siteLink }}</a></li>

                            </ul>
                        </div>
                    </div>
                    <div class="col-right">
                        <div class="card">
                            <img src="../assets/img/dc-logo-bg.png" alt="">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </main>

</template>

<style lang="scss" scoped>
@use '../assets/scss/mixins' as*;
@use '../assets/scss/variables' as*;

* {
    color: #FFF
}

.row-button {
    @include center-flex;

    button {
        margin-top: 80px;
        width: 140px;
        height: 30px;
        background-color: dodgerblue;
        font-size: 12px;
        cursor: pointer;
    }
}



main {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    background-repeat: no-repeat;
}

#comics {
    overflow: hidden;
    padding: 30px;
    height: 60%;

}


section ul {
    @include center-flex;
    gap: 100px
}

.col-left li a {
    font-size: 10px;
    color: $light-grey;
}



section {
    @include center-flex;
    background-color: dodgerblue;
    height: 150px;
    width: 100%;
    color: white;

}

#contents {
    width: 100%;
    min-height: 500px;
    font-size: 25px;
    background-color: #242424;
    padding: 20px
}

#contents .container {
    display: flex;
    justify-content: flex-start;
    align-items: center;
}

a {
    color: #fff
}

.comic-row {
    display: flex;
    flex-wrap: wrap;
}



.row {
    width: 100%;
    height: 400px;
    @include center-flex;
}

.col-left {
    width: 50%;
    height: 380px;
    /* border: 2px dashed blue; */
    display: flex;
    justify-content: flex-start;
    align-items: center;

}

.s-column li a,
.m-column li a,
.e-column li a {
    display: inline-block;
    font-size: 15px;
    margin-bottom: 3px;

}


.col-right {
    width: 50%;
    /* border: 2px dashed blue; */
    position: relative;

}

.col-right img {
    position: absolute;
    top: -280px;
    right: 100px;
    width: 100%;
    z-index: 0;
}

.card {
    width: 60%;

}



.s-column,
.m-column,
.e-column {
    width: 30%;
    height: 100%;
}

h3 {
    margin: 15px 0
}

/* HOVER */
.s-column li a:hover,
.m-column li a:hover,
.e-column li a:hover {
    color: dodgerblue
}
</style>