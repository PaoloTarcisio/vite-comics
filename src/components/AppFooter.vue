<script>

export default {
        data() {
            return {
                footerLists : {

                    dcComics : [
                        "dc comics",
                        {
                        text: "characters",
                        },
                        {
                        text: "comics",
                        },
                        {
                        text: "movies",
                        },
                        {
                        text: "tv",
                        },
                        {
                        text: "games",
                        },
                        {

                        text: "videos",
                        },
                        {
                        text: "news",
                        }
                    ],

                    shop: [
                        "shop",
                        {
                        text: "Shop DC",
                        },
                        {
                        text: "Shop DC Collectibles",
                        }
                    ],

                    dc: [
                        "dc",
                        {
                        text: "Terms Of Use",
                        },
                        {
                        text: "Privacy Policy (New)",
                        },
                        {
                        text: "Ad Choices",
                        },
                        {
                        text: "Advertising",
                        },
                        {
                        text: "Jobs",
                        },
                        {
                        text: "Subscriptions",
                        },
                        {
                        text: "Talent Workshops",
                        },
                        {
                        text: "CPSC Certificate",
                        },
                        {
                        text: "Rating",
                        },
                        {
                        text: "Shop Help",
                        },
                        {
                        text: "Contact Us",
                        }
                    ],

                    sites: [
                        "sites",
                        {
                        text: "DC",
                        },
                        {
                        text: "Mad Magazine",
                        },
                        {
                        text: "DC Kids",
                        },
                        {
                        text: "DC Universe",
                        },
                        {
                        text: "DC Power Visa",
                        }
                    ]
                    },

                    socials : [
                    {
                        name: "Facebook",
                        image: "/img/footer-facebook.png",
                    },
                    {
                        name: "Twitter",
                        image: "/img/footer-twitter.png",
                    },
                    {
                        name: "YouTube",
                        image: "/img/footer-youtube.png",
                    },
                    {
                        name: "Pinterest",
                        image: "/img/footer-pinterest.png",
                    },
                    {
                        name: "Periscope",
                        image: "/img/footer-periscope.png",
                    },
                    ]
            }
        }
    };

</script>

<template>
    <footer>
        <section class="footer-top">
            <div class="container">
                <div v-for="(list, listTitle) in footerLists" :key="listTitle" class="p-3">
                    <h3>{{ list[0] }}</h3>
                    <ul>
                        <li v-for="(item, i) in list.slice(1)" :key="i" class="p-1">
                            {{ item.text }}
                        </li>
                    </ul>
                </div>
            </div>
        </section>

        <section class="footer-bottom p-3">
            <div class="container">
                <div class="d-flex w-100 justify-content-between">
                    <div>
                        <button>
                            <h3>sing up now!</h3>
                        </button>
                    </div>
                    <!-- <div class="socials">
                        <div class="d-flex align-content-center justify-content-between">
                            <div class="follow-us p-2">

                            </div>
                            <h3>
                                follow us
                            </h3>
                            <div v-for="social in socials">
                                <div class="single-social p-2">
                                    <img :src="social.image" alt="social image">
                                    <div class="social-name">
                                        {{ social.name }}
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div> -->
                </div>
            </div>
        </section>
    </footer>



</template>

<style lang="scss" scoped>
    footer
    {
        background-image: url("/img/footer-bg.jpg");
        background-size: contain;
        min-height: 450px;

        .container
        {
            color: white;
            display: flex;
            justify-content: space-evenly;
            h3
            {
                text-transform: uppercase;
            }

            ul
            {
                list-style: none;
                padding: 0;

                li
                {
                    color: lightgrey;
                }

                li:hover
                {
                    color: #0282F9;
                }
            }

        }

        .footer-bottom
        {
            background-color: #303030;
            .container
            {
                display: flex;
                justify-content: space-between;
                
                button
                {
                    h3
                    {
                        text-transform: uppercase;
                    }
                }

                .socials
                {
                    color: #0282F9;

                    img
                    {
                        color: grey;
                    }
                }
            }
        }
    }

</style>