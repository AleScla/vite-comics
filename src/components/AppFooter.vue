<script>
export default {
  data(){
    return{
        firstCol: [
                'Characters',
                'Comics',
                'Movies',
                'TV',
                'Games',
                'Videos',
                'News',
            
        ],
        secondCol:[
            'Terms Of Use',
            'Privacy policy (New)',
            'Ad Choices',
            'Advertising',
            'Jobs',
            'Subscriptions',
            'Talent Workshops',
            'CPSC Certificates',
            'Ratings',
            'Shop Help',
            'Contact Us',
        ],
        thirdCol:[
            'DC',
            'MAD Magazine',
            'DC Kids',
            'DC Universe',
            'DC Power Visa'
        ],
        logos:[
            '/img/footer-facebook.png',
            '/img/footer-periscope.png',
            '/img/footer-pinterest.png',
            '/img/footer-twitter.png',
            '/img/footer-youtube.png',

        ]

    };
  },
}
</script>

<template>
    <footer>
        <section class="top-footer ">
            <div class="container">
                <div class="row ">
                    <div class="col-2 py-4">
                        <h4 class="py-2">
                          DC COMICS
                        </h4>
                        <ul>
                            <li v-for="links in firstCol" :key="index">
                                <a href="#">{{ links }}</a>
                            </li>
                        </ul>
                        <h4 class="py-2">
                            SHOP
                        </h4>
                        <ul>
                            <li>
                                <a href="#"> Shop DC</a>
                                
                            </li>
                            <li>
                                <a href="#"> Shop DC Collectibles</a>
                            </li>
                        </ul>
                    </div>
                    <div class="col-2 py-4">
                        <h4 class="py-2">
                          DC 
                        </h4>
                        <ul>
                            <li v-for="links in secondCol" :key="index">
                                <a href="#">{{ links }}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="col-2 py-4">
                        <h4 class="py-2">
                          SITES 
                        </h4>
                        <ul>
                            <li v-for="links in thirdCol" :key="index">
                                <a href="#">{{ links }}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="col-6 py-4 logo-side">
                        <img src="/public/img/dc-logo-bg.png" alt="BG">
                    </div>
                </div>
            </div>
        </section>
        <section class="bottom-footer">
            <div class="container">
                <div class="row">
                    <div class="col py-4">
                        <div class="sign-up btn">
                            <a href="#">
                                <h5>
                                    SIGN-UP NOW!
                                </h5>
                            </a>
                        </div>
                    </div>
                    <div class="col bottom-r-footer justify-content-end align-items-center d-flex ">
                        <a href="#">
                            <h3 class="m-0 pe-2">
                                FOLLOW US
                            </h3>
                        </a>
                        <ul class="nav justify-content-end h-100 align-items-center">
                            <li class="nav-item " v-for="logo in logos" :key="index">
                                <a class="nav-link" href="#">
                                    <img :src="logo" alt="logos">
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
    </footer>
</template>

<style lang="scss" scoped>
  .top-footer{
    background-image:url('./public/img/footer-bg.jpg');
    width:100%;
    background-size: cover;
    .container{
        .row{
            .col-2{
                color:white;
                ul{
                    list-style:none;
                    padding:0;
                    li{
                        padding-bottom:5px;
                        a{
                            color:#b3b3b3;
                            text-decoration:none;
                        }
                    }
                }

            }
            .col-6.logo-side{
                position:relative;
                overflow:hidden;
                img{
                    position:absolute;
                    top:-30%;
                }
            }
        }
    }
  }
  .bottom-footer{
    background-color:#1C1C1C;
    .container{
        .row{
            .col{
                .sign-up.btn{
                    border:3px solid #0282F9;
                    a{
                        text-decoration:none;
                        color:white;
                        h5{
                            padding:9px;
                        }
                    }
                }
            }
            
            .bottom-r-footer{
                a{
                    text-decoration:none;
                    h3{
                        color:#0282F9;
                        font-weight:bold;
                    }
                }
                ul{
                    li{
                        a{
                            padding:5px 10px;
                        }
                    }
                }
            }
        
        }
    }

  }
</style>