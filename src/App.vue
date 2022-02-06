<template>
  <div id="app">
    <Header/>
    <Content/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Content from './components/content/Content.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Content,
    Footer,
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
  font-family: 'Roboto';
}
#App{
  widows: 100%;
}

.content-wrapper{
  width: 1170px;
}

.block-wrapper{
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

h1{
  font-size: 24px;
}

@font-face {
  font-family: "Roboto";
  src: local("Roboto"),
   url(./fonts/roboto/Roboto-Light.ttf) format("truetype");
}

</style>
