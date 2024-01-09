<script>
export default {
    name: 'AppMain',
    data() {
        return {
            comics: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book",
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel",
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel",
                },
            ]
        }
    }
}
</script>
<template lang="">
    <main>
        <div class="jumbotron"> 
            <img class="jumbotron-image" src="/img/jumbotron.jpg" alt="">
        </div>
        <div>
            <h5 class="jumbotron-heading">current series</h5>
        </div>
        <div class="boxes cont-comics">
            <div class="comics-card" v-for="comic, index in comics" :key="index">
                <div class="img-card">
                    <img :src="comic.thumb" alt="comic.series" />
                </div>
                <div class="text-comics text-light">{{ comic.series}}</div>
            </div>
        </div>
        <div class="d-flex justify-content-center">
            <button>
                Load More
            </button>
        </div>
    </main>
</template>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
@use '../styles/generals.scss' as *;
    

    .jumbotron {
        position: relative;
        width: 100%;
        height: 400px;
        overflow: hidden;
        object-fit: cover;
        .jumbotron-image {
            width: 100%;
            height: auto;
        }
    }
    .jumbotron-heading{
        font-weight: 700;
        position: absolute;
        bottom: 425px;
        left: 19%;
        color: white;
        text-transform: uppercase;
        background-color: $primary_color;
        padding: 10px 15px;
    }
    .boxes {
        cursor: pointer;
        margin-top: 2rem;
        display: flex;
        flex-wrap: wrap;

        .comics-card {
            width: 200px;
            margin: 15px 0;
            padding: 0 10px;
            overflow: hidden;

            .img-card {
            width: 200px; 
            height: 200px;
            }

            .text-comics {
                padding-top: 10px;
                text-transform: uppercase;
                text-align: center;
                font-size: 12px;
                font-weight: 700;
            }
            
            img {
                width: 100%;
                height: 100%;
                object-fit: cover;
                object-position: 50% 0%;
                &:hover{
                    opacity: 0.5;
                }
            }

        }
    }

    button {
        @include btn-load;

        &:hover {
            transition: all 0.3s ease-in-out;
            color: $primary_color;
            background-color: $secondary_color;
            border: 1px solid $secondary_color;
        }
    }

</style>