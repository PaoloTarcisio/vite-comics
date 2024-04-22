<script>

export default {
        data() {
            return {
                comics: [
                    {
                        "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                        "price": "$19.99",
                        "series": "Action Comics",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                        "price": "$3.99",
                        "series": "American Vampire 1976",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                        "price": "$16.99",
                        "series": "Aquaman",
                        "type": "graphic novel",
                    },
                    {
                        "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                        "price": "$2.99",
                        "series": "Batgirl",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                        "price": "$3.99",
                        "series": "Batman",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                        "price": "$2.99",
                        "series": "Batman Beyond",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                        "price": "$3.99",
                        "series": "Batman/Superman",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                        "price": "$4.99",
                        "series": "Batman/Superman Annual",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                        "price": "$5.99",
                        "series": "Batman: The Joker War Zone",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                        "price": "$6.99",
                        "series": "Batman: Three Jokers",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                        "price": "$4.99",
                        "series": "Batman: White Knight Presents: Harley Quinn",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                        "price": "$16.99",
                        "series": "Catwoman",
                        "type": "graphic novel",
                    },

                ],

                merchandise: [
                    {
                        url: "/img/buy-comics-digital-comics.png",
                        text: "digital comics"
                    },
                    {
                        url: "/img/buy-comics-merchandise.png",
                        text: "dc merchandise"
                    },
                    {
                        url: "/img/buy-comics-subscriptions.png",
                        text: "subscription"
                    },
                    {
                        url: "/img/buy-comics-shop-locator.png",
                        text: "comic shop locator"
                    },
                    {
                        url: "/img/buy-dc-power-visa.svg",
                        text: "dc power visa"
                    },
                ]
            }
        }
    }

</script>

<template>

    <main>
        <section class="jumbo">

        </section>

        <section class="comics-list">
            <div class="comics-container container p-3">
                <!-- current series -->
                <span class="current-series">
                    CURRENT SERIES
                </span>
                <div class="row p-3">
                    <div class="col-lg-3 col-md-4 col-sm-6" v-for="comic in comics">
                        <div class="comic-thumb p-3">
                            <img :src="comic.thumb" alt="">
                        </div>
                        <div class="comic-title px-3">
                            {{ comic.series }}
                        </div>
                    </div>
                </div>
            </div>
        </section>


        <section class="merchandise">
            <div class="container">
                <div class="merchandise-container p-5">
                    <div v-for="immagine in merchandise" class="merchandise-content px-3">
                        <div>
                            <span class="merchandise-img p-2">
                                <img :src="immagine.url" alt="Immagine merchandise">
                            </span>
                            <span class="merchandise-text pl-2">
                                {{ immagine.text }}
                            </span>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

</template>

<style lang="scss" scoped>


//sezione jumbotron
section.jumbo
{
    background-image: url("/public/img/jumbotron.jpg");
    min-height: 400px;
}

// sezione lista comics
section.comics-list
{
    background-color: #1C1C1C;
    .comics-container
    {
        .current-series
        {
            background-color: #0282F9;
            color: white;
            font-weight: 500;
            padding: 0.8rem 1.3rem;
            
        }

        .row
        {
            .comic-thumb
            {
                img
                {
                    height: 200px;
                    object-fit: contain;
                    margin: 0 auto;
                }
            }
            .comic-title
            {
                text-transform: uppercase;
                color: white;
            }
        }
    }
}




// sezione merchandise
.merchandise
{
    background-color: #0282F9;
    color: white;

    .merchandise-container
    {
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        margin: 0 auto;

        .merchandise-content
        {
            img
            {
                height:50px;
            }

            .merchandise-text
            {
                text-transform: uppercase;
            }
        }
    }
}
</style>
