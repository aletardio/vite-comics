<script>
export default {
    name: 'AppBlueSection',
    data() {
        return {
            blueSection: [
                {
                    name: 'digital comics',
                    url: '/img/buy-comics-digital-comics.png'
                },
                {
                    name: 'dc merchandise',
                    url: '/img/buy-comics-merchandise.png'
                },
                {
                    name: 'subscription',
                    url: '/img/buy-comics-subscriptions.png'
                },
                {
                    name: 'comic shop locator',
                    url: '/img/buy-comics-shop-locator.png'
                },
                {
                    name: 'dc power visa',
                    url: '/img/buy-dc-power-visa.svg'
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
                <div class="d-flex flex-row px-5" v-for="(section, index) in blueSection" :key="index">
                    <img class="icons my-1" :src="section.url" :alt="section.name" />  
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
            cursor: pointer;
            padding: 20px 10px;
            font-size: 12px;
            
        }
        img.icons {
            cursor: pointer;
            margin: 0 10px;
            width: 42px;
            height: 52px;
        }
    }

</style>