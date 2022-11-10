<template>
    <footer>
        <div class="first-footer">
            <div class="container">
                <div>
                    <div class="prima-lista">
                        <h3>Dc Comics</h3>
                        <ul>
                            <li><a href="#nogo">Characters</a></li>
                            <li><a href="#nogo">Comics</a></li>
                            <li><a href="#nogo">Movies</a></li>
                            <li><a href="#nogo">TV</a></li>
                            <li><a href="#nogo">Games</a></li>
                            <li><a href="#nogo">Videos</a></li>
                            <li><a href="#nogo">News</a></li>
                        </ul>
                    </div>
                    <div class="seconda-lista">
                        <h3>Shop</h3>
                        <ul>
                            <li><a href="#nogo">Shop DC</a></li>
                            <li><a href="#nogo">Shop DC Collectibles</a></li>
                        </ul>
                    </div>
                </div>
                <div class="terza-lista">
                    <h3>Dc</h3>
                    <ul>
                        <li><a href="#nogo">Term Of Use</a></li>
                        <li><a href="#nogo">Privacy policy (New)</a></li>
                        <li><a href="#nogo">Ad Choices</a></li>
                        <li><a href="#nogo">Advertising</a></li>
                        <li><a href="#nogo">Jobs</a></li>
                        <li><a href="#nogo">Subscription</a></li>
                        <li><a href="#nogo">Talent Workshops</a></li>
                        <li><a href="#nogo">CPSC Certificates</a></li>
                        <li><a href="#nogo">Ratings</a></li>
                        <li><a href="#nogo">Shop Help</a></li>
                        <li><a href="#nogo">Contact Us</a></li>
                    </ul>
                </div>
                <div class="quarta-lista">
                    <h3>Site</h3>
                    <ul>
                        <li><a href="#nogo">DC</a></li>
                        <li><a href="#nogo">MAD Magazine</a></li>
                        <li><a href="#nogo">DC Kids</a></li>
                        <li><a href="#nogo">DC Universe</a></li>
                        <li><a href="#nogo">DC Power Visa</a></li>
                    </ul>
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
    export default {
        name: 'FooterComponent'
    }
</script>

<style lang="scss" scoped>
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

                h3 {
                    color: $whitetext;
                    text-transform: uppercase;
                    margin-bottom: 10px;
                }
                ul {
                    list-style: none;
                    li a{
                        display: inline-block;
                        text-decoration: none;
                        color: $textgray;
                        @include dflex;
                        font-size: 0.9rem;
                        margin-bottom: 8px;
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