<template>
  <div class="container-about">
      <div class="image">
          
      </div>
      <div class="about-content">
            <h2>Um pouco sobre mim ...</h2>
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi consequatur labore cum molestiae  facilis aliquid iure illo debitis excepturi recusandae sequi in quaerat illum repudiandae perspiciatis suscipit! Ab, quibusdam.
                
            </p>
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
        flex-direction: row;
        justify-content: space-between;
        margin-top: 50px;
       

        .image{
            height: 300px;
            width: 350px;
            border-radius: 50%;
            margin-left: 50px;
            background-color: rgb(22, 35, 65);
        }

        .about-content{
            max-width: 60%;
            display: flex;
            flex-direction: column;
         
            height: 300px;
            margin: 30px 100px;
            h2{
                font-size: 65px;
                color: var(--secondary);     
            }
            p{
                margin-top: 30px;
                line-height: 35px;
                font-weight: 100;
                font-size: 20px;
                scan{
                    color: var(--sv);
                    font-weight: bold;
                }
            } 
        }
    }
</style>