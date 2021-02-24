<template>
    <div class="box">
        <div class="percent">
            <svg>
                <circle cx="70" cy="70" r="70"> </circle>
                <circle 
                :style="
                     StrokeDashoffsetValue
                    "
                cx="70" cy="70" r="70"> </circle>
            </svg>
            <div 
            class="number"
            >
                <h3>{{porcent}}<span>%</span></h3>
            </div>
        </div>
        <span class="title">{{title}}</span>
    </div>
</template>

<script>
export default {
    props:{
        title: {
            //required: true,
            type: String,
            default: "TITULO"
        },
        porcent: {
            required: true,
            type: Number
        }
    },
  data() {
      return {
         StrokeDashoffsetValue: {
             'stroke-dashoffset': 440 - (440 * this.porcent ) / 100 
         }
      }
  },
  
  
}
</script>

<style scoped lang="scss">

    //$porc: 0;

    .box {
        
        position: relative;
        width: 200px;
        height: 200px;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        margin-bottom: 40px;
        //background-color: red;
        //box-shadow: 0 30px 60px rgba($color: #000000, $alpha: .2);
        .percent{
            svg{
                position: relative;
                width: 150px;
                height: 150px;
            }

            svg circle{
                width: 150px;
                height: 150px;
                fill: none;
                stroke-width: 10;
                //stroke: var(--primary);
                transform: translate(5px,5px);
                stroke-dasharray: 440;
                stroke-dashoffset: 440;
                stroke-linecap: round;
                //animation-name: loadingSkill;
                
                &:nth-child(1){
                    stroke-dashoffset: 0;
                    stroke: var(--quaternary);
                }  

                &:nth-child(2){
                    //stroke-dashoffset: 440 - (440 * $porc) / 100;//calc(440 - (440 * $porc) / 100);
                    stroke: var(--sv);
                }    
            }
            
            .number{
                position: absolute;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;
                display: flex;
                justify-content: center;
                //align-items: center;
                margin-top: 25%;
                color: var(--tertiary);
                h3{
                    font-size: 48px;
                    span{
                        font-size: 24px;
                    }
                }
            
            }
        } 
        .title{
            margin-top: 20px;
            font-size: 20px;
            font-weight: bold;
            color: var(--tertiary);
        }
    }

    @keyframes loadingSkill {
        
        from{
            stroke-dashoffset: 440;
        }
        to{
            stroke-dashoffset: 880;
        }
    }

</style>