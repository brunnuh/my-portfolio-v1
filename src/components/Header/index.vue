<template>
    <header class="container">
        <div class="top">
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

        <div class="about-me">
            <h2>
                <p>Lorem ipsum</p> dolor sit amet consectetur, <p>adipisicing</p> elit. Deserunt fugiat unde  magnam officia <p>tempore</p> Voluptatem .
            </h2>
        </div>
    </header>
</template>



<style scoped lang="scss">
    .container{
        background-color: var(--primary);
        grid-area: HD;
        display: flex;
        flex-direction: column;
        color: var(--quinary);
        
        .top{
            display: flex;
            flex-direction: row;
            justify-content: space-around;
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
                margin-right: 10px;
                width: 90px;
                height: 30px;
                display: flex;
                align-items: center;
                justify-content: center;
                border-radius: 15px;
                transition:0.4s;
                
               
                &:hover{
                    cursor: pointer;
                  
                    //background: var(--sv);
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
            max-width: 65%;
            margin-top: 10vw;
            h2{
                font-size: 7.5vh;
                color: var(--quaternary);
                p{
                    display: inline;
                    background: -webkit-linear-gradient(right, var(--sv), var(--sv2));
                    -webkit-background-clip: text;
                    -webkit-text-fill-color: transparent;
                }
            }
        }
        
    }
</style>