<script>
export default {
    name: 'AppBlueSection',
    data() {
        return {
            blueSection: [
                {
                    name: 'digital comics',
                    url: '../assets/img/buy-comics-digital-comics.png'
                },
                {
                    name: 'dc merchandise',
                    url: '../assets/img/buy-comics-merchandise.png'
                },
                {
                    name: 'subscription',
                    url: '../assets/img/buy-comics-subscriptions.png'
                },
                {
                    name: 'comic shop locator',
                    url: '../assets/img/buy-comics-shop-locator.png'
                },
                {
                    name: 'dc power visa',
                    url: '../assets/img/buy-dc-power-visa.svg'
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
                    <img :src="section.url" :alt="section.name" />  
                    <div class="text-uppercase text-section">{{ section.name }}</div>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    @use '../styles/generals.scss' as *;
    @use '../styles/partials/variables' as *;

    .content {
        height: 100px;
        background-color: $primary_color;
    }

    .text-section {
        padding: 5px 10px;
        font-size: 15px;
    }
</style>