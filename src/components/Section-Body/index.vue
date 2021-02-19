<template>
    <section class="container">
        <AboutComponent />
    </section>
</template>

<script>
import AboutComponent from './About/index'
export default {
    components: {
        AboutComponent
    }
}
</script>

<style scoped lang="scss">
    .container{
        height: 500px;
        grid-area: BD;
        
    }
</style>