<template>
    <header>
        <div class="container">
            <div class="logo">
                <a href="#">
                    <img src="/public/img/dc-logo.png" alt="Logo DC">
                </a>
            </div>
            <nav>
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a :href="link.url" :class="{ 'active': link.current }">{{ link.text }}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
    export default {
        name: 'HeaderComponent',
        data() {
            return {
                links: [
                    {
                        text: "Characters",
                        url: "#nogo",
                        current: false,
                    },
                    {
                        text: "Comics",
                        url: "#nogo",
                        current: true,
                    },
                    {
                        text: "Movies",
                        url: "#nogo",
                        current: false,
                    },
                    {
                        text: "Tv",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Games",
                        url: "#nogo",
                        current: false,
                    },
                    {
                        text: "Collectibles",
                        url: "#nogo",
                        current: false,
                    },
                    {
                        text: "Videos",
                        url: "#nogo",
                        current: false,
                    },
                    {
                        text: "Fans",
                        url: "#nogo",
                        current: false,
                    },
                    {
                        text: "News",
                        url: "#nogo",
                        current: false,
                    },
                    {
                        text: "Shop",
                        url: "#nogo",
                        current: false,
                    },
                ],
            };  
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;

header {
    
    .container {
        @include dflex;
        
        ul {
                list-style: none;
                @include dflex;

                li {
                    font-weight: bold;
                    display: inline-block;
                    text-transform: uppercase;
                    margin-right: 20px;
                    font-size: 0.9rem;

                    a {
                        text-decoration: none;
                        color: $blacktext;
                        height: 50px;
                        padding-bottom: 50px;
                    

                        &.active,
                        &:hover {
                            color: $bluelink;
                            border-bottom: 5px solid $bluelink;
                        }
                    }
                }
            }
    }

    
}
</style>