<template lang="pug">
    nav.header__menu.menu
        ul.menu__list
            li.menu__item
                a.menu__link(href="#") Commercial
                ul.submenu__list
                    li.menu__item
                        a.menu__link(href="#") Lorem
                    li.menu__item
                        a.menu__link(href="#") Ipsum
                    li.menu__item
                        a.menu__link(href="#") Dores
                    li.menu__item
                        a.menu__link(href="#") Sit
            li.menu__item
                a.menu__link(href="#") Industrial
            li.menu__item
                a.menu__link(href="#") Infrastrusture
                ul.submenu__list
                    li.menu__item
                        a.menu__link(href="#") Lorem
                    li.menu__item
                        a.menu__link(href="#") Ipsum
                    li.menu__item
                        a.menu__link(href="#") Dores
                    li.menu__item
                        a.menu__link(href="#") Sit
            li.menu__item
                a.menu__link(href="#") Resources
            li.menu__item
                a.menu__link(href="#") Utilities
</template>

<style lang="sass" scoped>
    .menu
        &__list
            display: flex
            justify-content: flex-start
        &__item
            margin-left: 60px
            position: relative
            &:hover > .submenu__list
                visibility: visible
                opacity: 1
        &__item:first-child
            margin-left: 0
        &__link
            text-decoration: none
            color: #fff
            font-size: 15px
            line-height: 20px
            font-weight: 700
            transition: color .3s
            &:hover
                color: #154865
    .submenu__list
        visibility: hidden
        opacity: 0
        background: #ffffff63
        position: absolute
        width: 200px
        top: 15px
        left: 15px
        margin-top: 15px
        transition: opacity .3s
        &:before
            content: ''
            display: block
            height: 100%
            position: absolute
            top: -15px
            width: 100%
        .menu__item
            margin-left: 0
            padding: 10px
            border-bottom: 1px solid white
            transition: color .3s, background .3s
            &:hover
                background: #ffffffb3
                cursor: pointer
                & a
                    color: #154865

    @media (max-width: 1280px)
        .menu__list
            justify-content: flex-end

    @media (max-width: 960px)
        .menu
            &__item
                margin-left: 30px
            &__link--submenu::before
        left: calc(100% + 5px)

    @media (max-width: 768px)
        .header__menu
            visibility: hidden        
</style>
