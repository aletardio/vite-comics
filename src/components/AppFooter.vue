<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            footerLinks: [
                {
                    name: "dc comics", 
                    url: "#",
                    description: [
                        'Characters',
                        'Comics', 
                        'Movies', 
                        'TV', 
                        'Games', 
                        'Videos', 
                        'News'
                    ]
                },
                {
                    name: "dc", 
                    url: "#",
                    description: [
                        'Terms Of User',
                        'Privacy policy (New)', 
                        'Ad Choices', 
                        'Advertising', 
                        'Jobs', 
                        'Subscriptions', 
                        'Talent Workshops',
                        'CPSC Certificates',
                        'Ratings',
                        'Shop Help',
                        'Contact Us'
                    ]
                },
                {
                    name: "sites", 
                    url: "#",
                    description: [
                        'DC',
                        'MAD Magazine', 
                        'DC Kids', 
                        'DC Universe', 
                        'DC Power Visa', 
                    ]
                },
                {
                    name: "shop", 
                    url: "#",
                    description: [
                        'Shop DC',
                        'Shop DC Collectibles', 
                    ]
                },
            ],
            footerSocial: [
                {
                    name:'Facebook',
                    src:'../assets/img/footer-facebook.png'
                },
                {
                    name:'Twitter',
                    src:'../assets/img/footer-twitter.png'
                },
                {
                    name:'Youtube',
                    src:'../assets/img/footer-youtube.png'
                },
                {
                    name:'Pinterest',
                    src:'../assets/img/footer-pinterest.png'
                },
                {
                    name:'Periscope',
                    src:'../assets/img/footer-periscope.png'
                },
            ]

        }
    }
}
</script>
<template lang="">
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-6 d-flex flex-wrap">
                    <div class="col-4">
                        <div v-for="(link, index) in footerLinks" :key="index">
                            <div v-if="link.name == 'dc comics'">
                                <h4 class="text-uppercase text-light">{{ link.name }}</h4>
                                <ul class="size-title list-unstyled">
                                    <li v-for="(item, i) in link.description" :key="i">
                                        <a class="text-decoration-none" :href="link.url">{{ item }}</a>
                                    </li>
                                </ul>
                            </div>
                            <div v-if="link.name == 'shop'">
                                <h4 class="text-uppercase text-light">{{ link.name }}</h4>
                                <ul class="size-title list-unstyled">
                                    <li v-for="(item, i) in link.description" :key="i">
                                        <a class="text-decoration-none" :href="link.url">{{ item }}</a>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                    <div class="col-4">
                        <div v-for="(link, index) in footerLinks" :key="index">
                            <div v-if="link.name == 'dc'">
                                <h4 class="text-uppercase text-light">{{ link.name }}</h4>
                                <ul class="size-title list-unstyled">
                                    <li v-for="(item, i) in link.description" :key="i">
                                        <a class="text-decoration-none" :href="link.url">{{ item }}</a>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                    <div class="col-4">
                        <div v-for="(link, index) in footerLinks" :key="index">
                            <div v-if="link.name == 'sites'">
                                <h4 class="text-uppercase text-light">{{ link.name }}</h4>
                                <ul class="size-title list-unstyled">
                                    <li v-for="(item, i) in link.description" :key="i">
                                        <a class="text-decoration-none" :href="link.url">{{ item }}</a>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                
                </div>
                <div class="col-6">
                    <img class="logo-footer" src="../assets/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </div>
        <div class="row background-section">
            <div class="col-6 d-flex justify-content-start align-items-center ">
                <div class="margin-btn">
                    <button>
                        SIGN-UP NOW!
                    </button>
                </div>
            </div>
            <div class="col-6 d-flex justify-content-end align-items-center">
                <div class="d-flex flex-row px-5">
                    <span class="me-3">FOLLOW US</span>
                    <div v-for="(social, index) in footerSocial" :key="index">
                        <img :src="social.src">
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/generals.scss' as *;


    .col-6.d-flex.flex-wrap {
    padding-top: 20px;
    
    li {
        font-size: 10px;

        a{
            color: grey;
        }
    }

    }

    .logo-footer {
        width: 55%;
    }

    .background-section {
        background-color: #303030;
        height: 100px;
    }

    .margin-btn {
        padding: 0 215px;

        button {
            padding: 10px;
            color: $secondary_color;
            background-color: transparent;
            border: 3px solid $primary_color;
    
            &:hover{
                background-color: $primary_color;
                transition: background-color 0.700s;
            }
        }   
    }

    span {
        color: $primary_color;
        font-weight: 700;
    }


</style>