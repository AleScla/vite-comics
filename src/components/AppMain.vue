<script>
import SingleCard from './SingleCard.vue';
import AppJumbo from './AppJumbo.vue';
    export default {
        data(){
            return{
                utilities:[
                    {
                        src:'/img/buy-comics-digital-comics.png',
                        text: 'DIGITAL COMICS'
                    },
                    {
                        src:'/img/buy-comics-merchandise.png',
                        text: 'DC MERCHANDISE'
                    },
                    {
                        src:'/img/buy-comics-subscriptions.png',
                        text: 'SUBSCRIPTION'
                    },
                    {
                        src:'/img/buy-comics-shop-locator.png',
                        text: 'COMIC SHOP LOCATOR'
                    },
                    {
                        src:'/img/buy-dc-power-visa.svg',
                        text: 'DC POWER VISA'
                    },
                ],
                cards:[
      {
          thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
      },
      {
          thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
      },
      {
          thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
      },
      {
          thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
      },
      {
          thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
      },
      {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
      },
      {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
      },
      {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
      },
      {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
      },
      {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
      },
      {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
      },
      {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
      },
                ]
            }
        },
        components: {
            SingleCard,
            AppJumbo
        }
    }
</script>

<template>
    <main>
        <AppJumbo/>
        <section class="main-content">
            <div class="container">
                <div class="row">
                    <SingleCard v-for="(card, index) in cards" 
                    :key="index"
                    :card="card"/>
                </div>
                <div class="text-center text-white">
                    <span class="my-btn bg-primary d-inline-block">LOAD MORE</span>
                </div>
            </div>
        </section>
        <section class="utilities">
            <div class="container">
                <div class="row">
                    <div class="col-12">
                        <ul class="nav h-100 py-5 justify-content-around align-items-center">
                            <li class="nav-item" v-for="utility, index in utilities" :key="index">
                                <img class="pe-2" :src="utility.src" :alt="utility.text">
                                <span class="utilities-text">{{ utility.text }}</span>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

    </main>
</template>


<style lang="scss">
    main{
        .main-content{
            background-color:#1C1C1C;
            div.container{
                div.row{
                    div.col{
                        color:white;
                    }
                }
                div{
                    .my-btn{
                        padding:10px 40px;
                        margin-bottom:20px;
                        cursor:pointer;
                }
                }
            }
        }
        .utilities{
            background-color:#0282F9;
            .container{
                .row{
                    .col-12{
                        ul{
                            li{
                                img{
                                    width:80px;
                                    height:80px;
                                    object-fit:contain;
                                }
                                .utilities-text{
                                    color: white;
                                }
                            }
                        }
                    }
                }
            }
        }
    }
</style>

