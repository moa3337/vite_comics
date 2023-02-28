<script>
export default {
    components: { appLogo },
    props: {
        link: Array,
    },
};
</script>

<template>
    <footer>
        <appLogo :logo="link" />
        <div class="footer-1">
            <div class="list-box">
                <ul>
                    <h6>DC COMICS</h6>
                    <li><a href="">Characters</a></li>
                    <li><a href="">Comics</a></li>
                    <li><a href="">Movies</a></li>
                    <li><a href="">TV</a></li>
                    <li><a href="">Games</a></li>
                    <li><a href="">Videos</a></li>
                    <li><a href="">News</a></li>
                </ul>
                <ul class="foot-list">
                    <h6>DC</h6>
                    <li><a href="">Terms of Use</a></li>
                    <li><a href="">Privacy Policy (New)</a></li>
                    <li><a href="">Ad Choices</a></li>
                    <li><a href="">Advertising</a></li>
                    <li><a href="">Jobs</a></li>
                    <li><a href="">Subscriptions</a></li>
                    <li><a href="">Talent Workshops</a></li>
                    <li><a href="">Certificates</a></li>
                    <li><a href="">Ratings</a></li>
                    <li><a href="">Shop Help</a></li>
                    <li><a href="">Contact Us</a></li>
                </ul>
                <ul>
                    <h6>SITES</h6>
                    <li><a href="">DC</a></li>
                    <li><a href="">Mad Magazine</a></li>
                    <li><a href="">DC Kids</a></li>
                    <li><a href="">DC Universe</a></li>
                    <li><a href="">DC Power Visa</a></li>
                </ul>
                <br>
                <ul>
                    <h6>SHOP</h6>
                    <li><a href="">Shop DC</a></li>
                    <li><a href="">Shop DC Collectibles</a></li>
                </ul>

            </div>
        </div>
        <div class="footer-2">
            <div class="mynav">
                <button type="button" class="border border-3 border-primary">SIGN-UP NOW!</button>
                <div>
                    <h3>FOLLOW US</h3>
                    <div class="">
                        <img src="../assets/img/footer-bg.jpg" alt="">
                        <img src="../assets/img/footer-facebook.png" alt="">
                        <img src="../assets/img/footer-periscope.png" alt="">
                        <img src="../assets/img/footer-pinterest.png" alt="">
                        <img src="../assets/img/footer-bg.jpg" alt="">
                        <img src="../assets/img/footer-bg.jpg" alt="">
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss">
.footer-1 {
    background-image: url(../assets/img/footer-bg.jpg);
}

.list-box {
    width: 1000px;
    margin: 0 auto;
    display: flex;
    align-items: start;
}

.footer-2 {
    background-color: #303030;
}

h6 {
    color: white;
    margin-left: 4px;
}

h3 {
    color: #0282F9;
}

.li {
    list-style-type: none;
    margin-left: 0;
}

a {
    color: grey;
    font-size: 9px;
    margin: 7px 0;
}

button {
    color: white;
    padding: 8px;
    background-color: #303030;
}
</style>