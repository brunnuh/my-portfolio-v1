<template>
    <footer class="container-footer">
        <h3>
            &copy; {{getYear}} | created by Bruno Santos | All rights reserved
        </h3>
    </footer>
</template>

<script>
export default {
    computed:{
        getYear:() => {
            var nw = new Date;
            return nw.getFullYear();
        }
    }
}
</script>

<style scoped lang="scss">
    .container-footer{
        background-color: #f57921;
        grid-area: FT;
        display: flex;
        justify-content: center;
        align-items: center;
        color: var(--quinary);
    }
</style>