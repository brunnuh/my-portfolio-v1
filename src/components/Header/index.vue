<template>
    <header class="container">
        <div :class="[fixed ? 'spacing' : '']"></div>
        <div class="nav-bar" :class="[this.fixed ? 'fixedMain' : 'nav-bar-after']" v-scroll="menuFixed">
            
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
        </div>

        <div class="about-me" >
            <h2>
                <p>Lorem ipsum</p> dolor sit amet consectetur, <p>adipisicing</p> elit. Deserunt fugiat unde  magnam officia <p>tempore</p> Voluptatem .
            </h2>
        </div>
    </header>
</template>

<script>
export default {
    data() {
        return {
            fixed: false,
            positionNow: 0
        }
    },
    methods: {
        menuFixed: function(){
            //console.log("posicao atualizada descendo: ", this.positionNow, "posicaoY: ", window.scrollY)
            if(window.scrollY > 50){
                this.positionNow = window.scrollY
                this.fixed = true 
            }else if( window.scrollY < 100){
                this.fixed = false
            }
            
        }
    },
}
</script>


<style scoped lang="scss">
    .container{
        background-color: var(--primary);
        grid-area: HD;
        display: flex;
        flex-direction: column;
        
        color: var(--quinary);
       
        
        .fixedMain{
            position: fixed;
            background-color: var(--primary);
            opacity: 0.7;
            width: 100%;
            z-index: 101;
            animation-name: suavizar;
            animation-duration: 0.5s;
            
            //transition: transform 1s;
        }

        .spacing{
            height: 94px;
        }
        
        .nav-bar{
            
            display: flex;
            flex-direction: row;
            justify-content: space-around;
            padding-top: 20px; 
            
            .logo > a > img{
                width: 300px;
            }

            nav > ul {
                display: flex;
                margin-top: 15px;
            }

            nav > ul > li{
                list-style: none;
                margin-right: 10px;
                width: 90px;
                height: 30px;
                display: flex;
                align-items: center;
                justify-content: center;
                border-radius: 15px;
                transition: 0.4s;
                
               
                &:hover{
                    cursor: pointer;
                    a{
                        color: var(--sv);
                    }
                }
                a {
                    text-decoration: none;
                    color: var(--quinary);
                    font-weight: bolder;  
                    
                }
            }
        }
        .about-me{
            
            display: flex;
            align-self: center;
            justify-content: center;
            max-width: 65%;
            margin-top: 10vw;
            
            h2{
                font-size: 4.5vw;
                color: var(--quaternary);
                p{
                    display: inline;
                    background: -webkit-linear-gradient(right, var(--sv), var(--sv2));
                    background-clip: text;
                    -webkit-text-fill-color: transparent;
                }
            }
        }        
    }

    @keyframes suavizar {
        from{
            transform: translate(0%, -100%) matrix(1, 0, 0, 1, 0, 0) ;
        }

        to{
            transform: translate(0%, 0%) matrix(1, 0, 0, 1, 0, 0) !important;
        }
    }

    
    
</style>