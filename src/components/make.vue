<template>
    <div class="frase">
        <h1>Monte o seu hambúrger:</h1>
    </div>
    <div class="base">
        <div class="container">
            <div class="titulo">
                <h1>Escolha o pão: </h1>
            </div>
            <div class="descricao">
                <div v-for="pao in paes" :key="pao">
                    <input type="radio" id="pao" name="pao" :value="pao">
                    <label :for="pao">{{ pao }}</label>
                </div>
            </div>
        </div>
        <div class="container">
            <div class="titulo">
                <h1>Escolha a carne: </h1>
            </div>
            <div class="descricao">
                <div v-for="carne in carnes" :key="carne">
                    <input type="radio" :id="carne" name="carne" :value="carne">
                    <label :for="carne">{{ carne }}</label>
                </div>
            </div>
        </div>
        <div class="container">
            <div class="titulo">
                <h1>Escolha as saladas: </h1>
            </div>
            <div class="descricao">
                <div v-for="salada in saladas" :key="salada">
                    <input type="checkbox" :id="salada" name="salada" :value="salada">
                    <label for="salada">{{ salada }}</label>
                </div>
            </div>
        </div>
        <div class="container">
            <div class="titulo">
                <h1>Escolha os complementos: </h1>
            </div>
            <div class="descricao">
                <div v-for="complemento in complementos" :key="complemento">
                    <input type="checkbox" name="complemento" :id="complemento" :value="complemento">
                    <label for="complemento">{{ complemento }}</label>
                </div>
            </div>
        </div>
    </div>
    <div class="prosseguir_pedido">
        <button id="prosseguir">
            <div class="texto"> Prosseguir</div>
            <div class="seta">
                <img src="../assets/seta.png" alt="seta">
            </div>
        </button>
    </div>
</template>
<script>
export default{
    name: 'make',
    data(){
        return{
            paes : ["Integral", "Três queijos", "Brioche", "Pão com gergilim"],
            carnes : ["Picanha", "Alcatra", "Frango", "Maminha", "Costela"],
            saladas : ["Alface","Tomate","Cebola","Picles","Banana"],
            complementos : ["Bacon","Cheddar","Molho BBQ","Requeijão","Molho de alho"]
        }
    }
}
</script>
<style scoped>

    /*   BASE E CONTAINERS DE ITENS   */
    .base{
        display: flex;
        justify-content: space-around;
        align-items: center;
        height: 50vh;
    }
    .container{
        border: #703400 3px solid;
        border-radius: 10px;
        width: 20%;
        padding: 10px;
        min-height: 25vh;
    }
    .titulo{
        display: flex;
        height: 5rem;
        font-family:Verdana, Geneva, Tahoma, sans-serif;
        color: #a1d501;    
    }
    .descricao{
        font-family:Verdana, Geneva, Tahoma, sans-serif;
    }

    /*   BOTÃO PROSSEGUIR   */
    .prosseguir_pedido{
        display: flex;
        justify-content: center;
        align-items: center;
        height: 15vh;
    }
    #prosseguir{
        display: flex;
        cursor: pointer;
        justify-content: space-around;
        align-items: center;
        min-width: 15%;
        padding: 8px;
        border: none;
        border-radius: 10px;
        background-color:#ba6700;
    }
    .texto{
        font-family: Arial, Helvetica, sans-serif;
        font-size: 25px;
    }
    .seta{
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .seta img{
        max-width: 40px;
        max-height: 40px;
    }

    /*   FRASE INICIAL   */

    .frase{
        display: flex;
        justify-content: center;
        align-items: center;
        height: 8vh;
    }
    .frase h1{
        font-family: Arial, Helvetica, sans-serif;
        font-size: 35px;
    }


</style>
