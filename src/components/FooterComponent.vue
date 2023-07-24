<script>
import BarSearchComponent from './barSearchComponent.vue';

export default {
    components:{
        BarSearchComponent

    },
    data(){
        return {
        
            footerLinks:[
                {name:"dc comics",
                    links:["characters","comics","movies",
                    "TV","games","videos", "news"]
                },
                {name:"shop",
                    links:["shop dc","shop dc collectibles"]
                },
                {name:"dc",
                    links:["terms of use","privacy policy",
                    "ad choices","advertising","jobs","subscriptions",
                    "talent workshop","CPSC certificates","ratings","shop help",
                    "contact us"]
                },
                {name:"sites",
                    links:["DC","MAD magazine","DC kids","DC universe", "DC power visa"]}
            ],
            socials:["footer-facebook.png","footer-periscope.png","footer-pinterest.png","footer-twitter.png","footer-youtube.png"]

        }
    },
    methods:{

        getImgPath:function(imgPath){
            return new URL(imgPath,import.meta.url).href; 
        }
    }
}
</script>

<template>

    <BlueBarCmpnnt/>
    
    <section class="jumbotron">

        <div class="img-container">

            <img src="../assets/img/dc-logo-bg.png" alt="">

        </div>
        
        <div class="my-container"> 

            <nav class="left-jumbo-nav">
                
                <div v-for="(linksBlock,i) in footerLinks " :key=i>

                    <h4>
                        {{ linksBlock.name }}   
                    </h4>

                    <ul>

                        <li v-for="link in footerLinks[i].links">

                            <a href="nogo">
                                {{ link }}
                            </a>

                        </li>

                    </ul>

                </div>


            </nav>

        </div>
        
    </section>

    
    <section class="footer-bottom">

        <div class="my-container">

            <nav>

                <div class="sign-up">
                    sign-up
                </div>
    
           
                <div class="follow-us">

                    <h3>follow us</h3>

                    <ul>

                        <li v-for="singleSocial in socials">

                            <div class="img-container">
                                
                                <img :src="getImgPath(`../assets/img/${singleSocial}`)" alt="">

                            </div>

                        </li>

                    </ul>

                </div>
    
            </nav>

        </div>
    
    </section>


</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables.scss' as *;


.my-container{
    height: 100%;
}
.jumbotron{
    position: relative;
    height: 50vh;
    background-image: url(../assets/img/footer-bg.jpg);
    .img-container{
        position: absolute;
        top: 0;
        left: 0;
        overflow-y: hidden;
        height: 100%;       
        width: 100%; 
        img{
            position: absolute;
            left: 70%;
            top: 50%;
            transform: translate(-50%,-50%);
            height: 70vh;
        }
    }
    .left-jumbo-nav{
        width: 50%;
        max-height:100%;
        display:flex;
        flex-direction: column;
        justify-content: flex-end;
        align-items: flex-start;
        flex-wrap: wrap;
        flex-shrink: 1;
        flex-grow: 0;

        >div{
            max-width: calc(70% / 3);
            display:flex;
            flex-direction: column;
            flex-grow: 0;
            text-transform: capitalize;
            

            h4{
                color: white;
                margin: 0.5rem 0;
            }

            ul{
                list-style: none;
                padding-left: 0;
                font-size: small;

                li{ 
                    padding: 0.2rem;
                    a, a:visited{
                        color: $font-color-grey;
                    }
                }
            }
        }
    }
}

.footer-bottom{
    width: 100%;
    padding: 0.5rem 0;

    nav{
        display: flex;
        flex-wrap: wrap;
        width: 100%;
        justify-content: space-between;
        align-items: center;

        .sign-up{
            border: 2px solid $dc-blue;
            color: white;
            padding: 0.7rem;
        }

        .follow-us{
            max-width: 50%;
            display: flex;
            flex-wrap: wrap;
            flex-grow: 1;
            flex-shrink: 0;
            justify-content: space-between;
            align-items: center;

            h3{
                color: $dc-blue;
            }

            ul{
                list-style: none;
                display: flex;
                justify-content: space-between;
                align-items: center;
                flex-grow: 1;

                li{
                    flex-grow: 1;
                    flex-shrink: 0;
                    .img-container{
                        height: 2rem;
    
                        img{
                            height: 100%;
                        }
                    }
                }
            }

        }

    }
}

</style>