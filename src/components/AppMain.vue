<script>
export default {
    name: "AppMain"
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
                            <h5>DC COMICS</h5>
                            <ul>
                                <li>Characters</li>
                                <li>Comics</li>
                                <li>Movies</li>
                                <li>TV</li>
                                <li>Games</li>
                                <li>Collectibles</li>
                                <li>Videos</li>
                                <li>Fans</li>
                                <li>News</li>
                            </ul>
                            <h5>SHOP</h5>
                            <ul>
                                <li>Shop Dc</li>
                                <li>Shop Dc Collectibles</li>

                            </ul>
                        </div>
                        <div class="m-column">
                            <h5>DC </h5>
                            <ul>
                                <li>Characters</li>
                                <li>Comics</li>
                                <li>Movies</li>
                                <li>TV</li>
                                <li>Games</li>
                                <li>Collectibles</li>
                                <li>Videos</li>
                                <li>Fans</li>
                                <li>News</li>
                            </ul>
                        </div>
                        <div class="e-column">
                            <h5>SITES</h5>
                            <ul>
                                <li>Characters</li>
                                <li>Comics</li>
                                <li>Movies</li>
                                <li>TV</li>
                                <li>Games</li>
                                <li>Collectibles</li>
                                <li>Videos</li>
                                <li>Fans</li>
                                <li>News</li>
                            </ul>
                        </div>
                    </div>
                    <div class="col-right">
                        <div class="card">
                            <img src="../../public/img/dc-logo-bg.png" alt="">
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
    height: 100vh;
    background-image: url(../public/img/footer-bg.jpg);
    background-size: contain;
    background-repeat: no-repeat;
}

#comics {
    overflow: hidden;
    padding: 30px;
    height: 38%;
}


section ul {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 100px
}

ul li {
    font-size: 10px;
    color: #b1b1b1
}

section {
    background-color: dodgerblue;
    height: 100px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;

}

#contents {
    width: 100%;
    height: 80px;
    display: flex;
    justify-content: left;
    align-items: center;
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
    top: -175px;
    right: 100px;
    width: 60%;
    z-index: 0;
}

.s-column {
    width: 20%;
    height: 100%;
}

.m-column {
    width: 20%;
    height: 100%;
}

.e-column {
    width: 20%;
    height: 100%;
}

h5 {
    margin: 10px 0
}
</style>