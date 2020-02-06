<template lang="pug">
    header.header
        .header__wrap.wrap
            .logo
                a(href="/")
                    img(src="@/assets/logo.png" alt="Logo")
            <Menu />
            .header__main
                .header__title
                    | I want to feel what you wanted.
                .header__text
                    | Trent from punchy pint when lets get some snag. Get a dog up ya moolah piece of piss trent from punchy slaps. Shazza got us some chuck a sickie heaps he hasn't got a kindie. As stands out like bush telly with as stands out like porky. She'll be right pretty spiffy trent from punchy cab sav.
</template>

<script>
    import Menu from '@/components/Menu'
    export default {
        components: {
            Menu
        }
    }
</script>

<style lang="sass" scoped>
    .header
        background: url("./../assets/header-bg.png") top center fixed no-repeat #fff
        background-size: cover
        position: relative
        &::after
            content: ''
            width: 100%
            height: 100px
            background: url("./../assets/after-header.png")
            position: absolute
            bottom: 0
        &__wrap
            max-width: 968px
            margin: 0 auto
            padding-top: 55px
        &__main
            padding-top: 18%
            padding-bottom: 39.2%
            height: 260px
            text-shadow: 1px 1px 3px rgba(56, 103, 93, .7)
            width: 50%
        &__title
            font-size: 52px
            line-height: 62px
            font-weight: 300
            padding-bottom: 40px
        &__text
            font-size: 16px
            line-height: 27px
    .logo
      position: absolute
      top: 25px
      left: 25px
      &:hover
          animation: heartbeat 3s ease-in-out infinite both
    @keyframes heartbeat
        from
            transform: scale(1)
            transform-origin: center center
            animation-timing-function: ease-out
        10%
            transform: scale(0.91)
            animation-timing-function: ease-in
        17%
            transform: scale(0.98)
            animation-timing-function: ease-out
        33%
            transform: scale(0.87)
            animation-timing-function: ease-in
        45%
            transform: scale(1)
            animation-timing-function: ease-out

    @media (max-width: 1280px)
        .header__main
            padding:
                top: 10%
                bottom: 20%

    @media (max-width: 960px)
        .header__main
            width: 100%

    @media (max-width: 768px)
        .header
            &__wrap
                padding-top: 25px
            &__main
                padding-top: 20%
                padding-bottom: 10%
            &::after
                display: none
            &__title
                font-size: 40px
                line-height: normal
                padding-bottom: 0

    @media (max-width: 380px)
        .header__text
            font-size: 16px
            line-height: normal

</style>
