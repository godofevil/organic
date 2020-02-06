<template lang="pug">
    main.main
        .main__wrap.wrap
            .main__left
                .left__quote
                    p.quote__mark "
                    | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec leo nisi, feugiat vel placerat vitae, vulputate ac nibh. Ut scelerisque quis nulla sed tempor.
                    p.quote__mark.quote__mark--close "
                .left__controls
                    button.controls__button &#60;

                    button.controls__button &#62;

            .main__right
                .right__title
                    | Lorem ipsum dolor sit amet consectetur
                .right__text
                    | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec leo nisi, feugiat vel placerat vitae, vulputate ac nibh. Ut scelerisque quis nulla sed tempor. Maecenas viverra leo sed risus laoreet rutrum. Praesent lobortis ultrices vestibulum. Mauris rhoncus sagittis elit, a congue justo eleifend adipiscing. Ut pulvinar dignissim ante, at mollis justo laoreet et. Vestibulum viverra purus ligula, in placerat sapien condimentum nec. In diam nulla, pharetra dapibus molestie vitae, luctus a ante.
                    Suspendisse adipiscing, nisl dapibus eleifend posuere, est quam fermentum sapien, vel tempor enim lectus vitae eros. Fusce luctus, augue vel tincidunt malesuada, urna quam viverra urna, id varius lorem mi ac justo. Cras cursus quam nec diam sollicitudin, in laoreet felis scelerisque. Donec gravida tellus ut placerat gravida. Pelle
</template>

<style lang="sass" scoped>
    $color-orange: #fe992a
    .main
        &__wrap
            max-width: 968px
            display: grid
            grid-template-columns: 310px auto
            grid-column-gap: 60px
            padding-top: 80px
            padding-bottom: 110px
        &__left
            border-right: 1px solid #eaeaea
            padding-right: 45px
    .left
        &__quote
            font-size: 20px
            line-height: 28px
            color: $color-orange
            font-style: italic
        &__controls
            text-align: right
            font-size: 0
    .quote
        &__mark
            font-size: 48px
            line-height: 28px
            font-family: lato
            &--close
                padding-left: 90%
    .controls
        &__button
            width: 30px
            height: 30px
            background: $color-orange
            border: 0
            color: #fff
            margin-right: 5px
            font-family: Quicksand
            cursor: pointer
            transition: background .3s            
            &:hover
                background: lighten($color-orange, 20%)
    .right
        &__title
            font-size: 24px
            line-height: 14px
            color: $color-orange
            padding-bottom: 30px
        &__text
            font-size: 14px
            line-height: 28px
            color: #737c85
            font-family: Arial, sans-serif

    @media (max-width: 1280px)
        .main__wrap
            display: grid
            grid-template-columns: 310px auto
            grid-column-gap: 60px
            padding-top: 40px
            padding-bottom: 50px

    @media (max-width: 768px)
        .main
            &__wrap
                grid-template-columns: auto
                padding-top: 35px
            &__left
                border-right: none
                padding-right: 0
        .left__controls
            padding-bottom: 50px
        .right
            &__title
                line-height: normal
            &__text
                line-height: 23px
</style>
