<script>

export default {
    name: 'AppHeader',
    data() {
        return {
            links: [
                {
                    label:'Characters',
                    url: '#',
                    current: 'false'
                },
                {
                    label:'Comics',
                    url: '#',
                    current: 'true'
                },
                {
                    label:'Movies',
                    url: '#',
                    current: 'false'
                },
                {
                    label:'Tv',
                    url: '#',
                    current: 'false'
                },
                {
                    label:'Games',
                    url: '#',
                    current: 'false'
                },
                {
                    label:'Collectibles',
                    url: '#',
                    current: 'false'
                },
                {
                    label:'Videos',
                    url: '#',
                    current: 'false'
                },
                {
                    label:'Fans',
                    url: '#',
                    current: 'false'
                },
                {
                    label:'News',
                    url: '#',
                    current: 'false'
                },
                {
                    label:'Shop',
                    url: '#',
                    current: 'false'
                },
            ]
        }
    },
}
</script>
<template lang="">
    <header>
        <div class="container">
            <div class="row">
                <div class="col-4">
                    <a href="/" class="brand">
                        <img src="../assets/img/dc-logo.png" alt="">
                    </a>
                </div>
                <div class="col-8">
                    <nav>
                        <ul>
                            <li v-for="(link, index) in links" ::key="index">
                            <a :class="link.current ? 'active' : ''" :href="link.url"></a>
                            {{ link.label }}
                            </li>
                        </ul>
                    </nav>
                </div>
            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>

    header {
        margin: 20px 0;

        ul {
            display: flex;
            flex-direction: row;
            justify-content: center;
            padding: 35px 0;
        }

        li {
            color: rgb(125, 125, 125);
            text-transform: uppercase;
            list-style: none;
            padding: 0 15px;
            font-size: 13px;
        }
    }

</style>