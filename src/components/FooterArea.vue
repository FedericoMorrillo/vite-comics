<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <!--background di sfondo-->
    <footer>

        <!--sezione link utili e informazioni-->
        <div class="usefull-links flex">

            <!--contenitore link-->
            <div class="box flex">
                <div class="col"></div>
                <div class="col"></div>
                <div class="col"></div>

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
}

//contenitore
.usefull-links {
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

        }
    }

    // contenitore links 

    .bg-image {
        width: 35.2rem;
        height: 35.2rem;
        background-image: url("../assets/dc-logo-bg.png");
        position: relative;
        top: -100px;
    }
}
</style>