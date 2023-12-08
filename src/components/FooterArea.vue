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



    </footer>
    <!--/background di sfondo-->
</template>

<style scoped lang="scss">
//utils
.flex {
    display: flex;
}

//utils

footer {
    background-image: url("../assets/footer-bg.jpg");
    object-fit: cover;


    //contenitore
    .container {
        height: 23.125rem;
        max-width: 81.25rem;
        width: 80%;
        margin: 0 auto;
        justify-content: space-between;

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
                    padding-bottom: .1875rem;

                    a {
                        text-decoration: none;
                        color: #887a7c;
                        font-size: .75rem;

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
            height: 29.375rem;
            background-image: url("../assets/dc-logo-bg.png");
            position: relative;
            top: -100px;
        }

        //background logo
    }

    //contenitore


}
</style>