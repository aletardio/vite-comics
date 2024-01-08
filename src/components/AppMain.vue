<script>
export default {
    name: 'AppMain',
    data() {
        return {
            
        }
    }
}
</script>
<template lang="">
    <main>
        <div class="container">
            <h3>
            Content goes here
            </h3>
        </div>
    </main>
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/generals.scss' as *;
    

    .container {
        height: 100px;

        h3 {
            padding: 10px 0;
            color: $secondary_color;
        }
    }

</style>