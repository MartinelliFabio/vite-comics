<template>
    <main>
        <div class="container">
            <div class="main-content">
                <h1> --> Content goes here &lt;-- </h1>
            </div>
        </div>
    </main>
</template>

<script>
    export default {
        name: 'MainComponent'
    }
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;

main {
    background-color: $blacktext;
    
    .container {
        height: 150px;
        @include dflex;
        
        .main-content {
            color: $whitetext;
        }
    }
}
</style>