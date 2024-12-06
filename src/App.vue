<script setup>
//aqui teremos a lógica
//função, imports, variáveis
import coracao from "./assets/coracao.png";
import curtida from "./assets/curtida.png";
import {ref} from "vue";

const imagem = ref([coracao,coracao,coracao]);

const coracaoNaoCurtido = coracao;
const coracaoCurtido = curtida;

const alternarImagem = (index) => {
  if(imagem.value[index] === coracaoNaoCurtido){
    imagem.value[index] = coracaoCurtido    
  }else{
    imagem.value[index] = coracaoNaoCurtido
  }
}

</script>

<template>
  <header>
    <h1><span>CodeLab</span>Vue</h1>
    <input type="text" placeholder="Pesquisar no blog">
  </header>
  <main>
    <section>
      <div>
        <p>17 de ago, 2024</p>
        <!-- diretivas são atribututos HTML especiais do Vue-->
        <!-- para renderizar um dado da lógica (tudo que estiver detro do script), se for em uma tag (ex. tag p) usaremos as {{  }}. Como src, href é um atributo usaremos o v-bind, : é o atalho do v-bind -->
        <img :src="imagem[0]" alt="coração para dar 'curtida' na publicação" @click="alternarImagem(0)">
      </div>
      <h3>O que é linguagem de programação? Conheça as principais</h3>
      <p class="texto">Uma das mais populares vertentes da tecnologia da informação, a área de programação segue tendo muita demanda de trabalho justamente pela velocidade com que dispositivos tecnológicos vêm avançando.</p>
    </section>
    <section>
      <div>
        <p>12 de jul, 2024</p>
        <img :src="imagem[1]" alt="coração para dar 'curtida' na publicação" @click="alternarImagem(1)">
      </div>
      <h3>GitHub agora permite fazer login sem precisar de senha</h3>
      <p class="texto">O GitHub anunciou nesta quarta-feira (12) o acesso a partir das passkeys, método de autenticação sem senhas. A novidade está disponível em uma versão beta pública e pode substituir a autenticação em dois fatores.</p>
    </section>
    <section>
      <div>
        <p>21 de jun, 2024</p>
        <img :src="imagem[2]" alt="coração para dar 'curtida' na publicação" @click="alternarImagem(2)">
      </div>
      <h3>Por que os hiperlinks são azuis em sua maioria?</h3>
      <p class="texto">Quem navega na internet, certamente já percebeu que ela conta com diversos recursos para tornar a nossa vida mais fácil. Entre essas opções podemos mencionar os hiperlinks - uma palavra ou termo clicável que direciona o leitor.</p>
    </section>
  </main>
  <!--tags, ou seja tudo que será renderizado na tela-->
</template>

<style scoped lang="scss">
/* todo estilo */

header{
  background-color:#17171A;
  color:#E07B67;
  height: 20vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-family: "Space Grotesk", sans-serif;
  font-weight: 500;

  input{
    width: 40vw;
    height: 4vh;
    padding: 8px 8px;
    border-radius: 8px;
    background-color: #202024;
    border: 2px solid #252529;
    color: #AFABB6;
  }

  h1{
    margin-bottom: 1%;

    span{
      color: #FFFFFF;
    }
  }

};

main{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #121214;
  height: 80vh;
}

section{
  display: flex;
  flex-direction: column;
  width: 40vw;
  background-color: #202024;
  margin: 1% 0%;
  padding: 2% 2%;
  border-radius: 8px;
  border: 2px solid #252529;
  transition: all 0.3s ease;

  &:hover{
    border: 2px solid #E07B67;
  }
}

div{
  display: flex;
  justify-content: space-between;
  font-family: "Inter", serif;
  font-weight: 500;
  color: #E07B67;
  font-size: 0.8rem;

  img{
    cursor: pointer;
  }
}

h3{
  font-family: "Space Grotesk", serif;
  color: #FFFFFF;
  margin-bottom: 1%;
  font-weight: 500;
}

.texto{
  font-family: "Inter", serif;
  color: #AFABB6;
  font-weight: 500;
  font-size: 0.9rem;
}
</style>
