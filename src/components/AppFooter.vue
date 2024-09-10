<script>
export default {
  data(){
    return{

    };
  },
}
</script>

<template>
    <footer>
        <section class="top-footer py-4">
            <div class="container">
                <div class="row">
                    <div class="col-2">
                        <h4>
                         TITOLO
                        </h4>
                        <ul>
                            <li>
                                ABC
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
        <section class="bottom-footer">

        </section>
    </footer>
</template>

<style lang="scss" scoped>
  .top-footer{
    background-image:url('./public/img/footer-bg.jpg');
    .container{
        .row{
            .col-2{
                color:white;
                ul{
                    list-style:none;
                    padding:0;
                    li{
                        color:#b3b3b3;
                    }
                }

            }
        }
    }
  }
</style>