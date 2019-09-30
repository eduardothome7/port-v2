<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <h1>Eduardo Thomé</h1>
    <p>{{ msg }}</p>

    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
      <div v-for='section in sections'>
        <h3>{{ section.nome }}</h3>
        <div v-for='item in section.items'>
          <h4>{{ item.nome }}</h4>
          <p>{{ item.description }}</p>
        </div>
      </div>

  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  data: function(){
    return {
      msg: 'Portfólio V2',
      sections: [{
        nome: 'Conhecimentos',
        items: [
          {nome:'PHP', description: 'Laravel, Cakephp, Lumen. Instalação, configuração e customização de Magento, Wordpress'},
          {nome: 'Mobile', description: 'Android, Ionic'},
          {nome: 'Front-end', description: 'Angular, Vue.js, jQuery, Gulp. Design de Layouts'}
        ]
      },
      {
        nome: 'Formação',
        items: [
          {
            nome: 'Análise e Desenvolvimento de Sistemas - Senac', description: 'Jul/2012 - Jul/2016'
          },
          {
            nome: 'Pós Graduação em Desenvolvimento de Dispositivos Móveis - Senac', description: 'Mar/2017 - Jun/2019',
          }
        ],
      },
      {
        nome: 'Experiência',
        items: [
          {
            nome: 'Estúdio Sis', description:'Desenvolvedor PHP - FullStack. Mar/2017 - presente'
          },
          {
            nome: 'Rage Integrativa - estágio', description:'Desenvolvedor Front-end. Nov/2015 - Jul/2016'
          },
          {
            nome: 'ADP Brasil - estágio', description:'Desenvolvedor Progress 4GL. Set/2014 - Set/2015'
          },
          { 
            nome: 'Dell Computadores - estágio', description:'Suporte de Produção. Mai/2013 - Mai/2014'
          }
        ]
      }
      ]
    }
  }
  // components: {
    // HelloWorld
  // }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
