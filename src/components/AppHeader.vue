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

        <div class="container">
            
            <div>
                <img src="/img/dc-logo.png" alt="logo">
            </div>
    
            <ul>
                <li v-for="sezioni in HeaderMenu"
                >
                    <a href="#">
                        {{sezioni}}
                    </a>
    
                </li>
            </ul>
        </div>
    </header>

</template>

<style lang="scss" scoped>

    header {
        .container {
            display: flex;
            justify-content: space-between;

            ul {
            list-style: none;
            display: flex;
            align-items: center;

                li {
                    padding: 15px;

                    a {
                        text-decoration: none;
                        text-transform: uppercase;
                        color: grey;
                        font-weight: 800;
                    }
                }
            }

        }

        
    }

</style>
