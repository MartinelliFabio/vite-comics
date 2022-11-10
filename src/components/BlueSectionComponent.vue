<template>
    <section>
        <div class="container">
            <ul>
                <li v-for="(img, index) in blueImgs" :key="index">
                    <a :href="img.url">
                        <img :src="img.img" :alt="img.text" class="logo-blue">
                        <span>{{ img.text }}</span>
                    </a>
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'BlueSectionComponent',
        data() {
            return {
                blueImgs: [
                    {
                        img: '/public/img/buy-comics-digital-comics.png',
                        text: 'digital comics',
                        url: '#nogo'
                    },
                    {
                        img: '/public/img/buy-comics-merchandise.png',
                        text: 'dc merchandise',
                        url: '#nogo'
                    },
                    {
                        img: '/public/img/buy-comics-subscriptions.png',
                        text: 'subscription',
                        url: '#nogo'
                    },
                    {
                        img: '/public/img/buy-comics-shop-locator.png',
                        text: 'comic shop locator',
                        url: '#nogo'
                    },
                    {
                        img: '/public/img/buy-dc-power-visa.svg',
                        text: 'dc power visa',
                        url: '#nogo'
                    },
                ]
            }
        },
    }
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;

section {
    background-color: $bluelink;
    

    ul {
        list-style: none;
        @include dflex;
        height: 150px;
        padding: 0 25px;

        li a {
            display: inline-block;
            text-decoration: none;
            text-transform: uppercase;
            color: $whitetext;
            @include dflex;
            font-size: 0.9rem;

            .logo-blue {
                height: 6vh;
            }

            span {
               margin-left: 10px; 
            }
        }
    }
}
</style>