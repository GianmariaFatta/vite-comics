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

<style lang="scss" scoped>
@use '../assets/scss/mixins' as*;
@use '../assets/scss/variables' as*;

footer {
    @include center-flex;
    background-color: $mouse-grey;
    height: 135px;
    position: relative;
    z-index: 1;
}

.row {
    display: flex;
    width: 1200px;
}

.s-footer {
    @include left_flex;
    width: 100%;
}

.e-footer {
    @include right_flex;
    width: 100%;
}

button {
    height: 50px;
    width: 150px;
    border: 3px solid dodgerblue;
    background-color: transparent;
    color: #fff;
    font-size: 17px;

    a {
        color: #fff
    }
}


.socials {
    @include right_flex;
    margin-left: 20px;
    gap: 20px;
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