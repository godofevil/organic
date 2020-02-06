<template lang="pug">
    .container
        <Header />
        <Main />
        <Footer />
        <Responsive />
</template>

<script>
    import Header from '@/components/Header'
    import Main from '@/components/Main'
    import Footer from '@/components/Footer'
    import Responsive from '@/components/Responsive'

    export default {
        name: 'app',
        components: {
            Header,
            Main,
            Footer,
            Responsive
        }
    }
</script>

<style lang ="sass">
    @import url('https://fonts.googleapis.com/css?family=Lato:300,400,700&display=swap');
    @import url('https://fonts.googleapis.com/css?family=Quicksand:700&display=swap');
    @import url('http://allfont.ru/allfont.css?fonts=droid-serif-bold');
    
    *
        margin: 0
        padding: 0
    html
        scroll-behavior: smooth
    body
        font-family: lato, Arial, sans-serif
        font-size: 16px
        color: #fff
        overflow-wrap: break-word
    ul
        list-style-type: none
    a
        text-decoration: none
    .container
      max-width: 100%
      min-width: 320px
    .wrap
      max-width: 1550px
      min-width: 290px
      padding: 0 15px
      margin: 0 auto
</style>
