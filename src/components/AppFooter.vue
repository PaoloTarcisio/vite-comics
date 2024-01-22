<script>

export default {
        data() {
            return {
                merchandise: [
                    {
                        url: "img/buy-comics-digital-comics.png",
                        text: "digital comics"
                    },
                    {
                        url: "img/buy-comics-merchandise.png",
                        text: "dc merchandise"
                    },
                    {
                        url: "img/buy-comics-shop-locator.png",
                        text: "subscription"
                    },
                    {
                        url: "img/buy-comics-subscriptions.png",
                        text: "comic shop locator"
                    },
                    {
                        url: "img/buy-dc-power-visa.svg",
                        text: "dc power visa"
                    },
                ],
                DcComics: [
                    "Characters",
                    "Comics",
                    "Movies",
                    "TV",
                    "Games",
                    "Videos",
                    "News"
                ],
                Shop: [
                    "Shop DC",
                    "Shop DC Collectibles"
                ],
                DC: [
                    "Terms Of Use",
                    "Privacy Policy",
                    "Ad Choices",
                    "Advertising",
                    "Jobs",
                    "Subscriptions",
                    "Talnet Workshop",
                    "CPSC Certificates",
                    "Ratings",
                    "Shop Help",
                    "Contact Us"
                ],
                Sites: [
                    "DC",
                    "MAD Magazine",
                    "DC Kids",
                    "DC Universe",
                    "DC Power Visa"
                ],
            }
        }
    }

</script>

<template>

    <footer>
        <div class="container">
            <ul>
                <li
                v-for="(immagine, i) in merchandise">

                    <img :src="immagine.url" alt="immagine-merchandise">
                    <div class="merchandise-text">
                        {{ immagine.text }}
                    </div>

                </li>
            </ul>
        </div>
    </footer>

</template>

<style lang="scss" scoped>

    .container{
        background-color: #0282F9;

        ul {
            height: 200px;
            display: flex;
            justify-content: space-evenly;
            align-items: center;
            list-style: none;


            li {

                display: flex;
                align-items: center;

                .merchandise-text {
                    text-transform: uppercase;
                    color: white;
                }

                img:not(:last-child){
                    scale: 0.6;
                }
            }
        }
    }
</style>
