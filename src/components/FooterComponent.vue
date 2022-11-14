<template>
    <footer>
        <div class="first-footer">
            <div class="container">
                <div class="box-list">             
                    <ListLinksFooter v-for="(item, index) in footerLinks" :key="index" :obj="item" />
                </div>
                <div>
                    <img src="../../public/img/dc-logo-bg.png" alt="DC Logo Background">
                </div>
            </div>
        </div>
        <div class="second-footer">
            <div class="container">
                <div>
                    <button>sign-up now!</button>
                </div>
                <div class="social">
                    <span>follow us</span>
                    <img src="../../public/img/footer-facebook.png" alt="Facebook">
                    <img src="../../public/img/footer-twitter.png" alt="Twitter">
                    <img src="../../public/img/footer-youtube.png" alt="YouTube">
                    <img src="../../public/img/footer-pinterest.png" alt="Pinterest">
                    <img src="../../public/img/footer-periscope.png" alt="Periscope">
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
import { footerLinks } from '../data/comics'
import ListLinksFooter from './ListLinksFooter.vue'

    export default {
        name: 'FooterComponent',
        components: {
            ListLinksFooter
        },
        data() {
            return {
                footerLinks: footerLinks
            }
        }
    }
</script>

<style lang="scss">
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;

    footer {
        .first-footer {
            background: url('../../public/img/footer-bg.jpg') no-repeat;
            background-size: cover;
            overflow-y: hidden;

            .container {
                @include dflex;
                height: 50vh;

                .box-list {
                    display: flex;
                    flex-flow: wrap;

                    .list {
                        width: calc(100% / 3);
                    }
                    
                    .list:last-child {
                        margin-top: -50px;
                    }
                }

                h3 {
                    color: $whitetext;
                    text-transform: uppercase;
                    margin-bottom: 15px;
                }
                ul {
                    list-style: none;
                    li a{
                        display: inline-block;
                        text-decoration: none;
                        color: $textgray;
                        @include dflex;
                        font-size: 0.9rem;
                        margin-bottom: 4px;
                    }
                }
                
            }
        }
        .second-footer {
            background-color: $bgfooter;
            

            .container {
                @include dflex;
                height: 100px;

                button {
                    border: 2px solid $bluelink;
                    background-color: $bgfooter;
                    padding: 15px;
                    font-size: 1.1rem;
                    text-transform: uppercase;
                    color: $whitetext;
                }
                .social {
                    @include dflex;
                    
                    span {
                        color: $bluelink;
                        font-weight: bold;
                        text-transform: uppercase;
                        font-size: 1.2rem;
                    }
                    span,
                    img {
                        margin-right: 20px;
                    }

                }
            }
        }
    }
</style>