<script>
export default {
    data() {
        return { //array dei link per il menù dell' header
            sections: [
                {
                    name: "CHARACTERS",
                    link: "#",
                },
                {
                    name: "COMICS",
                    link: "#",
                },
                {
                    name: "MOVIES",
                    link: "#",
                },
                {
                    name: "TV",
                    link: "#",
                },
                {
                    name: "GAMES",
                    link: "#"
                },
                {
                    name: "COLLECTIBLES",
                    link: "#",
                },
                {
                    name: "VIDEOS",
                    link: "#",
                },
                {
                    name: "FANS",
                    link: "#",
                },
                {
                    name: "NEWS",
                    link: "#",
                },
                {
                    name: "SHOP",
                    link: "#",
                },
            ]
        }
    }
};
</script>

<template>
    <header>

        <!--contenitore header-->
        <div class="container flex">

            <!--logo-->
            <div class="logo flex">
                <img src="../assets/dc-logo.png" alt="logo">
            </div>
            <!--/logo-->

            <!--barra di navigazione-->
            <ul class="flex">
                <li v-for="section in sections" class="flex">
                    <a href="">{{ section.name }}</a>
                </li>
            </ul>
            <!--/barra di navigazione-->

        </div>
        <!--/contenitore header-->

    </header>
</template>

<style lang="scss">
//utils
.flex {
    display: flex;
}

//utils

header {
    height: 120px;
    background-color: white;

    //contenitore

    a {
        text-decoration: none;
    }

    .container {
        max-width: 81.25rem;
        width: 80%;
        height: 100%;
        margin: 0 auto;
        justify-content: space-between;
        align-items: center;

        //logo
        .logo {
            width: 5rem;
            height: 5rem;

            img {
                width: 100%;
            }
        }

        //logo

        //nav
        ul {
            height: 100%;
        }

        li {
            font-size: 12px;
            font-weight: 600;
            list-style: none;
            margin: 0 .9375rem 0 .9375rem;
            align-items: center;

            &:hover {
                cursor: pointer;
                border-bottom: 5px solid #0282f9;

                a {
                    color: #0282f9;
                }
            }

            a {
                color: black;
            }
        }

        //nav

    }

    //contenitore
}
</style>