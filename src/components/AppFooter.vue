<script>
import FooterColumn from './FooterColumn.vue';

export default{
        name: "AppFooter",
        data(){
            return{
                columns:[
                    {
                        title:"ORDER ONLINE",
                        links:[
                            'Appetizers',
                            'Burgers',
                            'Pizza',
                            'Fries',
                            'Sides',
                            'Desserts',
                            'Beverages',
                            'Specials'
                        ]
                    },
                    {
                        title:"NAVIGATE",
                        links:[
                            'Home',
                            'Alternate Home',
                            'Menu',
                            'About',
                            'News',
                            'Contact Us',
                            'Cart',
                        ]
                    },
                    {
                        title:"INFORMATION",
                        links:[
                            'My Account',
                            'Terms Of Service',
                            'Privacy Policy',
                        ],
                        immagini:[
                            '/img/app-store-badge-200x67.png',
                            '/img/play-store-badge.png'
                        ]
                    },
                    {
                        title:"OPENING HOURS",
                        opening:[
                            {
                                giorno:"Mon - ",
                                ora:"10AM to 11PM"
                            },
                            {
                                giorno:"Tue - ",
                                ora:"10AM to 11PM"
                            },
                            {
                                giorno:"Wed - ",
                                ora:"10AM to 11PM"
                            },
                            {
                                giorno:"Thur - ",
                                ora:"10AM to 11PM"
                            },
                            {
                                giorno:"Fri - ",
                                ora:"10AM to 11PM"
                            },
                            {
                                giorno:"Sat - ",
                                ora:"10AM to 1AM"
                            },
                            {
                                giorno:"Sun - ",
                                ora:"11AM to 10PM"
                            },
                        ]
                    },
                    {
                        title:"VOUCHER",
                        immagini:['/img/footer-coupon-200x200.png']
                    }
                ],

            }
        },
        components:{
            FooterColumn
        }
    }
</script>

<template>
    <div id="background-container">
        <div id="container">
            <div id="links-container">
                <FooterColumn v-for="column in columns" :obj="column"></FooterColumn>
            </div>
            <div id="footer-sotto">
                <img src="/img/takeout-logo-2x-200x43.png" alt="">
                <div id="stay">Stay In The Loop</div>
                <div id="sign">Sign up to receive up to date news and offers directly in your inbox:</div>
                <form action="">
                    <input type="email" placeholder="you@email.com"><br>
                    <button>SUBSCRIBE</button>
                </form>
                <div id="icons">
                        <i class="fa-brands fa-facebook-f"></i>
                        <i class="fa-brands fa-twitter"></i>
                        <i class="fa-brands fa-instagram"></i>
                        <i class="fa-brands fa-linkedin-in"></i>
                        <i class="fa-brands fa-whatsapp"></i>
                        <i class="fa-brands fa-youtube"></i>
                        <i class="fa-regular fa-envelope"></i>
                    </div>
                <div id="copy">&copy; Copyright 2012 - 2020 | Avada Theme by <span style="color: white;">ThemeFusion</span>| All rights reserved | Powered by <span style="color: white;">WordPress</span></div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../scss/variables" as *;
#background-container{
        width:100%;
        background-image: url('/img/footer-background-scaled.jpg');
        background-size: cover;
        background-position-y: -200px;
    }
#container{
            margin:auto;
            max-width: 950px;
            padding-top: 57px;
        }
#links-container{
    display: flex;
    justify-content: space-around;
    gap:110px ;
}
#footer-sotto{
    padding-top: 37px;
    text-align: center;
    img{
        width: 100px;
    }
    #stay{
        color: #FBDB30;
        font-weight: bold;
        font-size: 1.3em;
        padding-top: 7px;
    }
    #sign{
        margin-top: 8px;
        font-size: 0.6em;
    }
    input{width:400px;
    border-radius: 10px;
    padding: 3px 7px;
    border: 1px solid black;
margin-top: 12px;}
}

button{
    @include bottone();
    width: 400px;
}

#icons{
    padding: 21px;
    font-size: 0.7em;
    i{
        cursor: pointer;
        margin-right: 9px;
    }
}
#copy{
    color:#FBDB30;
    font-weight: bold;
    font-size: 0.5em;
    padding-bottom: 140px;
}

</style>