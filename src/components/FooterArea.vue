<script>
export default {
    data() {
        return {
            dcComics: [
                {
                    name: "Characters",
                    link: "#",
                },
                {
                    name: "Comics",
                    link: "#",
                },
                {
                    name: "Movies",
                    link: "#",
                },
                {
                    name: "TV",
                    link: "#",
                },
                {
                    name: "Games",
                    link: "#",
                },
                {
                    name: "Videos",
                    link: "#",
                },
                {
                    name: "News",
                    link: "#",
                },
            ],
            stores: [
                {
                    name: "Shop DC",
                    link: "#",
                },
                {
                    name: "Shop DC Collectibles",
                    link: "#",
                },
            ],
            DcInfo: [
                {
                    name: "Terms of Use",
                    link: "#",
                },
                {
                    name: "Privacy policy (New)",
                    link: "#",
                },
                {
                    name: "Ad Choises",
                    link: "#",
                },
                {
                    name: "Advertising",
                    link: "#",
                },
                {
                    name: "Jobs",
                    link: "#",
                },
                {
                    name: "Subscriptions",
                    link: "#",
                },
                {
                    name: "Talent Workshops",
                    link: "#",
                },
                {
                    name: "CPSC Certificates",
                    link: "#",
                },
                {
                    name: "Ratings",
                    link: "#",
                },
                {
                    name: "Shop Help",
                    link: "#",
                },
                {
                    name: "Contact Us",
                    link: "#",
                },
            ],
            sites: [
                {
                    name: "DC",
                    link: "#",
                },
                {
                    name: "MAD Magazine",
                    link: "#",
                },
                {
                    name: "DC Kids",
                    link: "#",
                },
                {
                    name: "DC Universe",
                    link: "#",
                },
                {
                    name: "DC Power Visa",
                    link: "#",
                },
            ],
            socialIcon: [
                {
                    img: "../src/assets/footer-facebook.png",
                    name: "facebook",
                },
                {
                    img: "../src/assets/footer-twitter.png",
                    name: "twitter",
                },
                {
                    img: "../src/assets/footer-youtube.png",
                    name: "youtube",
                },
                {
                    img: "../src/assets/footer-pinterest.png",
                    name: "pinterest",
                },
                {
                    img: "../src/assets/footer-periscope.png",
                    name: "periscope",
                },

            ],
        }
    }
}
</script>

<template>
    <!--background di sfondo-->
    <footer>

        <!--sezione link utili e informazioni-->

        <div class="container flex">

            <!--contenitore link-->
            <div class="box flex">
                <div class="col">
                    <h3>DC COMICS</h3>
                    <ul>
                        <li v-for="info in dcComics">
                            <a :href="info.link">
                                {{ info.name }}
                            </a>
                        </li>
                    </ul>
                    <h3>SHOP</h3>
                    <ul>
                        <li v-for="shop in stores">
                            <a :href="shop.link">
                                {{ shop.name }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="col">
                    <h3>DC</h3>
                    <ul>
                        <li v-for="info in DcInfo">
                            <a :href="info.link">
                                {{ info.name }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="col">
                    <h3>SITES</h3>
                    <ul>
                        <li v-for="site in sites">
                            <a :href="site.link">
                                {{ site.name }}
                            </a>
                        </li>
                    </ul>
                </div>

            </div>
            <!--/contenitore link-->

            <!--logo DC background-->
            <div class="bg-image">
            </div>
            <!--/logo DC background-->

        </div>

        <!--/sezione link utili e informazioni-->

        <!--sezione social-->

        <!--background-->
        <div class="social">
            <!--/background-->

            <div class="container-social flex">

                <!--button-->
                <button class="sign-btn">
                    <a href="">SIGN-NOW!</a>
                </button>
                <!--/button-->

                <!--follow us section-->
                <div class=" align flex">
                    <h3 class="follow-us">
                        FOLLOW US
                    </h3>
                    <button class="icon" v-for="icon in socialIcon">
                        <img :src="icon.img" :alt="icon.name">
                    </button>
                </div>
                <!--/follow us section-->
            </div>
        </div>
        <!--/sezione social-->

    </footer>
    <!--/background di sfondo-->
</template>

<style scoped lang="scss">
//utils
.flex {
    display: flex;
}

.align {
    align-items: center;
}

//utils

footer {
    background-image: url("../assets/footer-bg.jpg");
    object-fit: cover;


    //contenitore
    .container {
        max-width: 81.25rem;
        width: 80%;
        margin: 0 auto;
        justify-content: space-between;
        position: relative;

        //contenitore links
        .box {
            padding: 2.5rem 0 3.125rem 0;

            .col {
                margin-right: 1.875rem;
                flex-direction: column;

                h3 {
                    color: white;
                    padding: 15px 0;
                }

                li {

                    list-style: none;
                    padding: .1875rem 0;

                    a {
                        text-decoration: none;
                        color: #887a7c;
                        font-size: .875rem;

                        &:hover {
                            color: white;
                        }
                    }
                }
            }
        }

        // contenitore links 

        //background logo
        .bg-image {
            width: 35.2rem;
            height: 35rem;
            background-image: url("../assets/dc-logo-bg.png");
            position: absolute;
            top: -100px;
            right: 0;
        }

        //background logo
    }

    //contenitore

    //social
    .social {
        background-color: #303030;
        position: relative;
        z-index: 1;

        .container-social {
            max-width: 81.25rem;
            width: 80%;
            margin: 0 auto;
            justify-content: space-between;

            .sign-btn {
                height: 3.125rem;
                width: 8.75rem;
                border: 2px solid #0282f9;
                margin: 1.875rem 0;
                background-color: #303030;

                a {
                    color: white;
                    text-decoration: none;
                    font-weight: 600;
                }
            }

            h3 {
                color: #0282f9;
            }

            .icon {
                width: 2.1875rem;
                height: 2.1875rem;
                margin-left: 1.25rem;
                background-color: #303030;
                border: none;

                img {
                    width: 100%;
                }

            }

        }


    }

    //social
}
</style>