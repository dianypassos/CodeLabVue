<script setup>
//aqui teremos a lógica
//função, imports, variáveis
import coracao from "./assets/coracao.png";
import curtida from "./assets/curtida.png";
</script>

<template>
  <header>
    <h1>Vue</h1>
    <input type="text">
  </header>
  <main>
    <section>
      <div>
        <p>17 de ago, 2024</p>
        <!-- diretivas -->
        <!-- para renderizar um dado da lógica (tudo que estiver detro do script), se for em uma tag (ex. tag p) usaremos as {{  }}. Como src, href é um atributo usaremos o v-bind, : é o atalho do v-bind -->
        <img :src="coracao" alt="coração curtido">
      </div>
      <h3>O que é linguagem de programação? Conheça as principais</h3>
      <p>Uma das mais populares vertentes da tecnologia da informação, a área de programação segue tendo muita demanda de trabalho justamente pela velocidade com que dispositivos tecnológicos vêm avançando.</p>
    </section>
    <section>
      <div>
        <p>12 de jul, 2024</p>
        <img :src="coracao" alt="">
      </div>
      <h3>GitHub agora permite fazer login sem precisar de senha</h3>
      <p>O GitHub anunciou nesta quarta-feira (12) o acesso a partir das passkeys, método de autenticação sem senhas. A novidade está disponível em uma versão beta pública e pode substituir a autenticação em dois fatores.</p>
    </section>
    <section>
      <div>
        <p>21 de jun, 2024</p>
        <img :src="coracao" alt="">
      </div>
      <h3>Por que os hiperlinks são azuis em sua maioria?</h3>
      <p>Quem navega na internet, certamente já percebeu que ela conta com diversos recursos para tornar a nossa vida mais fácil. Entre essas opções podemos mencionar os hiperlinks - uma palavra ou termo clicável que direciona o leitor.</p>
    </section>
  </main>
  <!--tags, ou seja tudo que será renderizado na tela-->
</template>

<style scoped lang="scss">
/* todo estilo */

header{
  background-color:#17171A;
  color:#E07B67;
};

</style>
