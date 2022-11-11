<template>
    <section>
        <div class="jumbo container">
            <span>current series</span>
        </div>
    </section>
    
</template>

<script>
    export default {
        name: 'JumboComponent'
    }
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;

section {
    background: url('../../public/img/jumbotron.jpg') no-repeat;
    background-size: cover;

    div.jumbo {
        position: relative;
        height: 300px;

        span {
            position: absolute;
            // left: 10px;
            bottom: -25px;
            padding: 10px 20px;
            background-color: $bluelink;
            text-transform: uppercase;
            color: $whitetext;
            font-weight: bold;
        }
    }
}
</style>