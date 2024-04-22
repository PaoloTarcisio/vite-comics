<script>

export default {
        data() {
            return {
                HeaderMenu: [
                    "character",
                    "comics",
                    "movies",
                    "tv",
                    "game",
                    "collectibles",
                    "videos",
                    "fans",
                    "news",
                    "shop"
                ]

            }
        }
    }

</script>

<template>

    <header>
        <div class="header-container">
            <div class="logo">
                <img src="/img/dc-logo.png" alt="logo">
            </div>
            <div class="header-menu">
                <div v-for="sezioni in HeaderMenu" class="single-button-header-menu d-flex">
                    <h6>
                        {{sezioni}}
                    </h6>
                </div>
            </div>
        </div>
    </header>

</template>

<style lang="scss" scoped>

    .header-container {
        width: 90%;
        margin: 0 auto;
        display: flex;

        .logo
        {
            width: 100px;

            .img
            {
                object-fit: contain;
            }
        }

        .header-menu
        {
            flex-grow: 1;
            display: flex;
            justify-content: space-evenly;
            align-items: center;
            font-size: large;
            font-weight: 500;
            text-transform: uppercase;
            
            .single-button-header-menu
            {
                height: 100%;

                h6
                {
                    align-self: center;
                }
            }
            .single-button-header-menu:hover
            {
                border-bottom: 10px solid #0282F9;
                color: #0282F9;
            }
        }
    }

</style>
