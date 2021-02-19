<template>
    <header class="container">
        <div class="logo">
            <a href=""><img src="@/assets/logo.png"  alt="logo"></a>
        </div>
        <nav>
            <ul>
                <li><a href="">Home</a></li>
                <li><a href="">Sobre</a></li>
                <li><a href="">Portfólio</a></li>
                <li><a href="">Contatos</a></li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
    .container{
        background-color: var(--primary);
        grid-area: HD;
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        color: var(--quinary);
        padding-top: 20px;


        .logo > a > img{
            width: 300px;
                       
        }

        nav > ul {
            display: flex;
            margin-top: 30px;
        }

        nav > ul > li{
            list-style: none;
            a {
                text-decoration: none;
                color: var(--quinary);
                margin-right: 30px;
                font-weight: bolder;
            }
        }
    }
</style>