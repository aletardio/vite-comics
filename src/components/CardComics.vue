<script>
export default {
    name:'CardComics',
    props: {
        dc_comic: Object
    }
}
</script>
<template lang="">

    
    <div class="comics-card">
        <div class="img-card">
            <img :src="`${dc_comic.thumb}`" alt="dc_comic.series" />
        </div>
        <div class="text-comics text-light">{{ dc_comic.series }}</div>
    </div>

</template>
<style lang="scss" scoped>
    @use '../styles/partials/mixins' as *;
    @use '../styles/partials/variables' as *;
    @use '../styles/generals.scss' as *;

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
    
    

</style>