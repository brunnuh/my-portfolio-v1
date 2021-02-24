<template>
  <div class="container-about">
        <div class="image">
            <img src="@/assets/img_vender.png" alt="">
        </div>
        <div class="about-content">
            <h2>ABOUT ME</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Magni iste est delectus. Tenetur dolore culpa veritatis ducimus? At doloribus accusamus soluta facere ab? Necessitatibus pariatur eligendi blanditiis facere, veritatis voluptatibus.</p>
            <p>Lorem ipsum dolor sit amet <span>consectetur</span>, adipisicing elit. Minima, neque! Sit, pariatur? Facere nobis aspernatur eius velit dolore officia, est exercitationem iste in, perspiciatis dolorum ratione cumque iusto. Laudantium, natus.</p>
            <p>Lorem ipsum dolor sit amet consectetur <span>adipisicing</span> elit. Minus nihil excepturi voluptatibus? Numquam, vero perferendis. Libero labore atque illum voluptate? Quibusdam quidem amet delectus optio! Natus libero magni deserunt dolore?</p>
        </div>
  </div>
</template>

<script>


export default {
   
}
</script>

<style scoped lang="scss">
    .container-about{
        display: flex;
        align-items: center;
        height: 1300px;
        width: 100%;
        background-color: var(--quinary);
        
        .image{
            display: flex;
            justify-content: center;
            align-items: center;
            //margin-top: 100px;
            height: 80%;
            width: 50%;
            border-radius: 10px;
            margin-left: 50px;
            background-color: rgb(250, 249, 249);
            //box-shadow: 4px 4px 10px rgba($color: #919191, $alpha: 0.5);
            img{ // efeito paralax
                height: 70%;
                //max-width: 750px;
                //perspective: 2px;
                //transform-style: preserve-3d;
            }
        }


        .about-content{
         
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 40vw;
            width: 80%;
            //background-color: var(--secondary);

            




            h2,p{
                padding: 0 150px;
            }

            h2{
                font-size: 4.5vw;
                color: var(--sv);
                margin-bottom: 40px;
                width: 100%;
            }
            p{
                align-items: flex-start;
                margin-bottom: 20px;
                color: var(--primary);
                font-weight: 300;
                font-size: 1.2vw;
                font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
                span{
                    font-weight: 900;
                    color: var(--sv);
                }
            }
        }
        
    }
</style>