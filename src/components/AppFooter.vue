<script>
export default {
    name: "AppFooter",
    data() {
        return {
            socialLinks: [
                "facebook",
                "twitter",
                "youtube",
                "pinterest",
                "periscope",
            ]
        }
    }
}
</script>

<template>
    <footer>
        <div class="footer-top">
            <div class="container">
                <div class="footer-top-inner">
                    <div class="footer-top-upper">
                        <div class="footer-top-menu">
                            <h3 class="footer-top-menu-title">DC COMICS</h3>
                            <ul>
                                <li><a href="#">Characters</a></li>
                                <li><a href="#">Comics</a></li>
                                <li><a href="#">Movies</a></li>
                                <li><a href="#">TV</a></li>
                                <li><a href="#">Games</a></li>
                                <li><a href="#">Videos</a></li>
                                <li><a href="#">News</a></li>
                            </ul>
                            <h3 class="footer-top-menu-title">SHOP</h3>
                            <ul>
                                <li><a href="#">Shop DC</a></li>
                                <li><a href="#">Shop DC Collectibles</a></li>
                            </ul>
                        </div>
                        <div class="footer-top-menu">
                            <h3 class="footer-top-menu-title">DC</h3>
                            <ul>
                                <li><a href="#">Terms Of Use</a></li>
                                <li><a href="#">Privacy policy (New)</a></li>
                                <li><a href="#">Ad Choices</a></li>
                                <li><a href="#">Advertising</a></li>
                                <li><a href="#">Jobs</a></li>
                                <li><a href="#">Subscriptions</a></li>
                                <li><a href="#">Talent Workshops</a></li>
                                <li><a href="#">CPSC Certificates</a></li>
                                <li><a href="#">Ratings</a></li>
                                <li><a href="#">Shop Help</a></li>
                                <li><a href="#">Contact Us</a></li>
                            </ul>
                        </div>
                        <div class="footer-top-menu">
                            <h3 class="footer-top-menu-title">SITES</h3>
                            <ul>
                                <li><a href="#">DC</a></li>
                                <li><a href="#">MAD Magazine</a></li>
                                <li><a href="#">DC Kids</a></li>
                                <li><a href="#">DC Universe</a></li>
                                <li><a href="#">DC Power Visa</a></li>
                            </ul>
                        </div>
                    </div>
                    <div class="footer-top-copy">
                        <p>All Site Content TM and © 2020 DC Entertainment, unless otherwise <a href="#">noted here</a>.
                            All rights reserved.</p>
                        <p>
                            <a href="#">Cookies Settings</a>
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="container">
                <div class="footer-bottom-left">
                    <a href="#" class="button cta">
                        Sign-up now!
                    </a>
                </div>
                <div class="footer-bottom-right">
                    <div class="social">
                        <h4 class="social-title uppercase">Follow us</h4>
                        <ul>
                            <li v-for="(item, index) in socialLinks" :key="index" :class="item">
                                <a href="#"></a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.footer-top {
    background-image: url('/images/footer-bg.jpg');
    background-size: cover;

    .footer-top-inner {
        padding: 40px 0;
        background-image: url('/images/dc-logo-bg.png');
        background-position: right;
        background-repeat: no-repeat;

        .footer-top-upper {
            @include flexbox(row, flex-start, flex-start);

            .footer-top-menu {
                padding-right: 30px;

                .footer-top-menu-title {
                    color: $footer_title_color;
                    font-size: 21px;
                    margin: 0 0 15px 0;
                }

                ul {
                    list-style-type: none;
                    margin: 0 0 20px 0;
                    padding: 0;

                    li {
                        margin: 4px 0;

                        a {
                            color: $footer_text_color;
                            font-size: 12px;

                            &:hover {
                                color: $main_color;
                            }
                        }
                    }
                }
            }
        }
    }

    .footer-top-copy {

        p {
            color: $footer_text_color;
            font-size: 12px;
            margin: 0;

            a {
                color: $main_color;
            }
        }
    }
}

.footer-bottom {
    background: $footer_bg_color;
    padding: 30px 0;

    .footer-bottom-left,
    .footer-bottom-right {
        float: left;
        width: 50%;
    }

    .cta {
        background: transparent;
        border: 2px solid $main_color;
        display: inline-block;
        font-family: "Open Sans", sans-serif;
        font-size: 16px;
        padding: 14px;
        transition: all 0.3s ease;

        &:hover {
            background: $main_color;
        }
    }

    .social {
        @include flexbox(row, flex-end, center);

        .social-title {
            color: $main_color;
            font-size: 22px;
            line-height: 50px;
            margin: 0 15px 0 0;
        }

        ul {
            list-style-type: none;
            margin: 0;
            padding: 0;

            li {
                display: inline-block;
                margin-left: 15px;

                &:hover {
                    opacity: 0.8;
                }
            }

            @each $icon in $footer_socials {
                li.#{$icon} {
                    background-image: url('/images/footer-#{$icon}.png');
                    background-repeat: no-repeat;
                    background-size: contain;
                }
            }

            a {
                display: inline-block;
                width: 35px;
                height: 35px;
            }
        }
    }
}
</style>