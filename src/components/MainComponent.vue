<template>
    <main>
        <div class="container">
            <div class="main-content">
                <div class="row">
                    <div class="card" v-for="(comic, index) in comics" :key="index">
                        <div class="img-box">
                            <img :src="comic.thumb" :alt="comic.series">
                        </div>
                        <p>{{comic.series}}</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="btn-box">
            <a href="#nogo"><button>Load more</button></a>
        </div>
    </main>
</template>

<script>
import {comics} from '../data/comics';

    export default {
        name: 'MainComponent',
        data() {
            return {
                comics: comics,
            }
        }
        
    }
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;

main {
    background-color: $bgblack;
    
    .container {
        padding-top: 3.5rem;
        padding-bottom: 8rem;

        .main-content {
            color: $whitetext;
            padding: 1rem;
            
            .row {
                display: flex;
                flex-wrap: wrap;
                row-gap: 50px;

                .card {
                    height: 200px;
                    width: calc(100% / 6);
                    
                    .img-box {
                        height: 95%;
                        overflow-y: hidden;
                    }

                    p {
                        margin-top: 15px;
                        width: 80%;
                    }
                }
            }
            
        }
    }
    .btn-box {
        display: flex;
        justify-content: center;

        button {
            border: 0;
            background-color: $bluelink;
            padding: 10px 55px;
            margin-bottom: 25px;
            text-transform: uppercase;
            color: $whitetext;
            font-weight: bold;
            cursor: pointer;
            transition: background 0.3s;

            &:hover {
                background-color: $bluetext;
            }
        }
    }
}
</style>