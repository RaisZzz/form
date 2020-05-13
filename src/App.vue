<template>
  <div id="app">
    <Header/>
    <Form/>
    <Footer/>
  </div>
</template>

<script>
    import Header from "./components/Header";
    import Form from "./components/Form";
    import Footer from "./components/Footer";

    export default {
        name: 'App',
        components: {Footer, Form, Header}
    }
</script>

<style lang="sass">
  *
    padding: 0
    margin: 0
    text-decoration: none
    list-style: none
    box-sizing: border-box
  body
    height: 100vh
    font-family: sans-serif
  #app
    height: 100%
    display: flex
    flex-direction: column
</style>