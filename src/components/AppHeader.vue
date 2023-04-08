<script>
export default {
    name: "AppHeader",
    data() {
        return {
            menuItems: [
                "Characters",
                "Comics",
                "Movies",
                "Tv",
                "Games",
                "Collectibles",
                "Videos",
                "Fans",
                "News",
                "Shop",
            ]
        }
    }

}
</script>

<template>
    <header>
        <div class="header-top">
            <div class="container">
                <nav>
                    <ul>
                        <li>
                        <a href="#">DC Power℠ Visa®</a>
                    </li>
                        <li>
                            <a href="#">Additional DC Sites ▼</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
        <div class="header-bottom">
            <div class="container">
                <div class="navbar">
                    <div class="logo">
                        <a href="#">
                            <img src="https://www.dccomics.com/sites/all/themes/dc_comics_bp/logo.png" alt="DC Comics logo">
                        </a>
                    </div>
                    <nav>
                        <ul>
                            <li v-for="(item, index) in menuItems" :key="index">
                                <a href="#">{{ item }}</a>
                            </li>
                            <!-- <li>
                                        <a href="#">Shop <span class="arrow-down">▾</span></a>
                                    </li> -->
                        </ul>
                    </nav>
                    <div class="search">
                        <input type="text" placeholder="Search">
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;
@use '../styles/partials/animations' as *;

header {

    ul {
        list-style-type: none;
        margin: 0;

        li {
            display: inline-block;

            a {
                display: inline-block;
                text-transform: uppercase;
            }
        }
    }

    .header-top {
        background-color: $main_color;

        nav {
            text-align: right;

            li {

                &:not(:last-child) {
                    margin-right: 60px;
                }

                a {
                    color: $main_bg_text_color;
                    font-size: 11px;
                    font-weight: 600;
                    line-height: 25px;
                }
            }
        }
    }

    .header-bottom {
        box-shadow: 0 1px 2px 0 #ebebeb;

        .navbar {
            @include flexbox(row, space-between, center);

            .logo {

                a {

                    img {
                        vertical-align: middle;
                        width: 80px;
                    }
                }
            }

            nav {

                a {
                    color: $nav_color;
                    font-family: $title_font_family;
                    font-size: 16px;
                    font-weight: 700;
                    line-height: 115px;
                    padding: 0 $nav_spacing;
                    position: relative;

                    &::after {
                        content: '';
                        position: absolute;
                        bottom: 0;
                        left: $nav_spacing;
                        width: calc(100% - (#{$nav_spacing} * 2));
                        height: 0;
                    }

                    &:hover,
                    &.active {
                        color: $main_color;

                        &::after {
                            animation: nav_item_decoration 0.3s ease;
                            height: 5px;
                            background: $main_color;
                        }
                    }

                    .arrow-down {
                        color: $main_color;
                        font-size: 100%;
                    }
                }
            }

            .search {

                input {
                    background-image: url("https://www.dccomics.com/sites/all/themes/dc_comics_bp/images/search-icon-new.png");
                    background-repeat: no-repeat;
                    background-position: right;
                    border: 0;
                    border-bottom: 2px solid $main_color;
                    font-family: "Open Sans Condensed", sans-serif;
                    font-size: 16px;
                    font-weight: 700;
                    outline: 0;
                    padding: 0 24px 4px 0;
                    text-align: right;
                    width: 110px;
                }

                ::-webkit-input-placeholder {
                    /* Edge */
                    color: $nav_color;
                }

                :-ms-input-placeholder {
                    /* Internet Explorer 10-11 */
                    color: $nav_color;
                }

                ::placeholder {
                    color: $nav_color;
                }
            }
        }
    }
}
</style>