<script>
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
                ]
            }
        }
    }
</script>

<template>
    <main>
        <section class="main-content">
            <div class="container">
                <div class="row">
                    <div class="col py-5 my-bg text-center">
                        <h1>CONTENT GOES HERE</h1>
                    </div>
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


<style lang="scss" scoped>
    main{
        .main-content{
            background-color:#1C1C1C;
            div.container{
                div.row{
                    div.col{
                        color:white;
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

