<template lang="pug">
  #app
    .logoTexto FCiencias
    img(id='escudo' :src ='fcescudo')
    .pruebaContenedor
      .cosa1.left.unamGoldColor Cosa1
      .cosa2.left.unamGoldColor.bold Cosa2

    div {{ this.mensaje }}
    div.delay.isClosed(:class="showMsg") {{ this.respuesta }}
    router-view
</template>

<script>
  import imageLogo from '@/assets/fcescudo.png'
  
  export default {
    name: 'App',
    data: function () {
      return {
        mensaje: 'Están listos chicos!!!',
        respuesta: 'Si capitán estamos listos',
        fcescudo: imageLogo
      }
    }
  }
</script>

<style  lang="scss" >
  //styles
  $goldUnam:#c5911e;

  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
    .logoTexto{
      font-family: "Arial Rounded MT Bold", "Helvetica Rounded", Arial, sans-serif;;
      text-transform: uppercase;
      display: block;
      font-size: 3rem;
      letter-spacing: 8px;
      color: #FFF;
      text-shadow: 0 2px 2px #5683D8 , 0px -2px 1px #F2F2F2;
      text-shadow: 0 2px 5px #c4b59d, 0px -2px 1px #fff;
      font-weight: bold;
      letter-spacing: -4px;
      text-align: center;
      background: linear-gradient(to bottom, #5683D8 0%, #6C96DE 100%);
      //background: linear-gradient(to bottom, #ece4d9 0%,#e9dfd1 100%);
      position: relative;
      padding: 20px 20px;
      top: 10%;
      left: 50%;
      transform: translate(-50%,-50%);
      border-radius: 0px;
    }
    .pruebaContenedor{
      width: 90%;
      border: 1px solid #193455;
      .unamGoldColor.bold{
        font-weight: 900;
      }
      .unamGoldColor{
        color:$goldUnam;
      &.bold{
        font-weight: 600;
      }

      }
    }
    #escudo{
      width:150px;
      height:auto;
    }



  }
</style>
