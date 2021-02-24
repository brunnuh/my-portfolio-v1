<template>
  <div class="container-skills">
      <h2>SKILLS</h2>

    <section class="skills">
        <div class="front-skills center-title">
            <h3>Front-End</h3>
            <CircleComponent title="HTML5" :porcent="70"/>
            <CircleComponent title="CSS3" :porcent="50"/>
        </div>
        <div class="back-skills center-title">
            <h3>Back-End</h3>
            <CircleComponent title="PHP" :porcent="60"/>
            <CircleComponent title="Python" :porcent="50"/>
            <CircleComponent title="Dart" :porcent="90"/>
        </div>
        <div class="frameworks-skills center-title">
            <h3>Frameworks</h3>
            <CircleComponent title="VueJs" :porcent="50"/>
            <CircleComponent title="Flutter" :porcent="90"/>
            <CircleComponent title="Laravel" :porcent="50"/>
        </div>
        <div class="others-skills center-title">
            <h3>Outros</h3>
            <CircleComponent title="SQL" :porcent="70"/>
          
        </div>
    </section>
  </div>
</template>

<script>
import CircleComponent from '@/components/globals/CircleProgress'
export default {
    components:{
        CircleComponent
    }
}
</script>

<style scoped lang="scss">
    .container-skills{
        width: 100%;
        height: 1200px;
        background-color: var(--primary);
        display: flex;
        flex-direction: column;
        //justify-content: center;
        align-items: center;
        h2{
            background: -webkit-linear-gradient(right, var(--sv), var(--sv2));
            background-clip: text;
            -webkit-text-fill-color: transparent;
            font-size: 4.5vw;
            margin-top: 100px;
            margin-bottom: 80px;
        }

        .center-title{
            display: flex;
            flex-direction: column;
            align-items: center;
        }


        // skills css
        .skills{
            //background-color: #fff;
            width: 100%;
            display: flex;
            justify-content: space-around;
            
            h3{
                color: var(--tertiary);
                margin-bottom: 50px;
                font-size: 30px;
            }


        }
    }
</style>