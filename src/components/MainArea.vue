<script>
export default {
    data() {
        return {
            // array info bar
            DcInformations: [
                {
                    img: "./src/assets/buy-comics-digital-comics.png",
                    desc: "DIGITAL COMICS",
                },
                {
                    img: "./src/assets/buy-comics-merchandise.png",
                    desc: "DC MERCHANDISE",
                },
                {
                    img: "./src/assets/buy-comics-subscriptions.png",
                    desc: "SUBSCRIPTION",
                },
                {
                    img: "./src/assets/buy-comics-shop-locator.png",
                    desc: "COMIC SHOP LOCATOR",
                },
                {
                    img: "./src/assets/buy-dc-power-visa.svg",
                    desc: "DC POWER VISA",
                },
            ]
        }
    }
};
</script>

<template>
    <main>


        <!--primo contenitore-->
        <div class="container flex">

            <!--current series-->
            <h3 class="tag-series">
                CURRENT SERIES
            </h3>
            <!--/current series-->
        </div>

        <div class="center flex">
            <!--load more button-->
            <button class="add-btn">
                <h4>LOAD MORE</h4>
            </button>
            <!--/load more button-->
        </div>
        <!--/primo contenitore-->

        <!--secondo contenitore-->
        <div class="info-bar flex">

            <button class="flex btn" v-for="DcInformation in DcInformations">

                <!--icona-->
                <div class="icon">
                    <img :src="DcInformation.img" :alt="DcInformation.desc">
                </div>
                <!--/icona-->

                <!--descrizione-->
                <div class="icon-desc">
                    {{ DcInformation.desc }}
                </div>
                <!--/descrizione-->

            </button>
        </div>
        <!--/secondo contenitore-->

    </main>
</template>

<!--specifichiamo l' utilizzo di scss-->
<style scoped lang="scss">
.flex {
    display: flex;
}

.center {
    justify-content: center;
}

main {
    color: white;
    background-color: #1c1c1c;
    position: relative;



    //main content
    .container {
        max-width: 81.25rem;
        width: 80%;
        margin: 0 auto;
        align-items: center;

        //current series
        .tag-series {
            padding: .625rem 1.875rem;
            position: absolute;
            top: -1.25rem;
            cursor: default;
            background-color: #0282f9;
            text-align: center;
        }

        //current series
    }

    //load more
    .add-btn {
        margin: 3.125rem 0 1.25rem 0;
        padding: .625rem 3.75rem;
        background-color: #0282f9;
        color: white;
        border: none;
        cursor: pointer;
    }

    //load more


    //main content

    //info bar
    .info-bar {
        padding: 50px 0;
        font-size: 12px;
        background-color: #0282f9;
        justify-content: center;
        margin: 0 auto;
        position: relative;
        z-index: 1;

        //button
        .btn {
            background-color: transparent;
            border: none;
            color: white;
            align-items: center;
            margin-right: 4.375rem;
            cursor: pointer;

            .icon {
                width: 3.75rem;
                height: 3.125rem;
                padding-right: .625rem;

                img {
                    width: 100%;
                    height: 100%;
                    object-fit: contain;
                }
            }
        }

        //button

    }

    //info bar

}
</style>