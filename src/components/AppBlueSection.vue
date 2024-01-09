<script>
export default {
    name: 'AppBlueSection',
    data() {
        return {
            blueSection: [
                {
                    name: 'digital comics',
                    url: '../public/img/buy-comics-digital-comics.png'
                },
                {
                    name: 'dc merchandise',
                    url: '../public/img/buy-comics-merchandise.png'
                },
                {
                    name: 'subscription',
                    url: '../public/img/buy-comics-subscriptions.png'
                },
                {
                    name: 'comic shop locator',
                    url: '../public/img/buy-comics-shop-locator.png'
                },
                {
                    name: 'dc power visa',
                    url: '../public/img/buy-dc-power-visa.svg'
                },
            ]
        }
    },
}
</script>
<template lang="">
    <div class="container-fluid">
        <div class="row">
            <div class="col-12 content d-flex justify-content-center align-items-center">
                <div class="d-flex flex-row" v-for="(section, index) in blueSection" :key="index">
                    <img class="icons" :src="section.url" :alt="section.name" />  
                    <div class="text-uppercase text-section text-light">{{ section.name }}</div>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    @use '../styles/generals.scss' as *;
    @use '../styles/partials/variables' as *;

    .content {
        height: 120px;
        background-color: $primary_color;
        .text-section {
            padding: 20px 10px;
            font-size: 12px;
            
        img.icons {
            width: 20%;
        }
        }
    }

</style>