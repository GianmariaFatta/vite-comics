<script>
export default {
    name: "AppFooter"
}

</script>

<template>
    <footer>
        <div class="container">
            <div class="row">
                <div class="s-footer">
                    <button>
                        <a href="">SIGN-UP NOW!</a>
                    </button>
                </div>
                <div class="e-footer">
                    <h3>FOLLOW US</h3>
                    <div class="socials">
                        <a href=""><img src="../assets/img/footer-facebook.png" alt=""></a>
                        <a href=""><img src="../assets/img/footer-twitter.png" alt=""></a>
                        <a href=""><img src="../assets/img/footer-youtube.png" alt=""></a>
                        <a href=""><img src="../assets/img/footer-pinterest.png" alt=""></a>
                        <a href=""><img src="../assets/img/footer-periscope.png" alt=""></a>
                    </div>
                </div>
            </div>
        </div>

    </footer>

</template>

<style>
footer {
    background-color: #303030;
    height: 135px;
    display: flex;
    align-items: center;


}

.row {
    display: flex;
    width: 1200px;
}

.s-footer {
    width: 100%;
    display: flex;
    justify-content: flex-start;
    align-items: center;
}

.e-footer {
    width: 100%;
    display: flex;
    justify-content: flex-end;
    align-items: center;
}

button {
    height: 50px;
    width: 150px;
    border: 3px solid dodgerblue;
    background-color: transparent;
    color: #fff;
    font-size: 17px;
}

button a {
    color: #fff
}

.socials {
    margin-left: 20px;
    gap: 20px;
    display: flex;
    justify-content: flex-end;
    align-items: center;
}


h3 {
    color: dodgerblue;

}

/* HOVER */

button:hover {
    background-color: dodgerblue;
    color: #fff;
}

.socials a img:hover {
    filter: brightness(10);
}
</style>