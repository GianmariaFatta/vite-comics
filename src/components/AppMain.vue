<script>
export default {
    name: "AppMain",
    data() {
        return {
            comicsLinks: ["Characters", "Comics", "Movies", "TV", "Games", "Collectibles", "Videos", "Fans", "News"],
            shopLinks: ["Shop DC", "Shop Dc Collectibles"],
            dcLinks: ["Terms Of Use", "Privacy policy (new)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshop", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"],
            sitesLinks: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "Dc Power Visa"],
        }
    }
}

</script>

<template>
    <main>
        <div class="container">
            <div id="contents">
                <a href="">
                    <h3>Contents goes here</h3>
                </a>
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

<style scoped>
* {
    color: #FFF
}

main {
    height: 700px;

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
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 100px
}

.col-left li a {
    font-size: 10px;
    color: #b1b1b1
}



section {
    background-color: dodgerblue;
    height: 150px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;

}

#contents {
    width: 100%;
    height: 130px;
    display: flex;
    justify-content: left;
    align-items: center;
    font-size: 25px;
    /* background-color: #1c1c1c; */


}

a {
    color: #fff
}

.row {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.col-left {
    width: 50%;
    height: 200px;
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

.card {
    width: 60%;

}

img {
    position: absolute;
    top: -200px;
    right: 100px;
    width: 100%;
    z-index: 0;
}

.s-column {
    width: 30%;
    height: 100%;
}

.m-column {
    width: 30%;
    height: 100%;
}

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