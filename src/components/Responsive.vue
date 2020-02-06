<template lang="pug">
    <div>
        .responsive__button(@click="menuVisible = true" v-if="!this.menuVisible")
            img(src="@/assets/menu.svg")
        transition(name="fade")
            .responsive__menu(v-if="this.menuVisible")
                .responsive__close(@click="menuVisible = false")
                    img(src="@/assets/close.svg")
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
    </div>
</template>

<script>
    export default {
        data() {
            return {
                menuVisible: false
            }
        }
    }
</script>

<style lang="sass" scoped>
    .fade-enter, .fade-leave-to
        opacity: 0
    .fade-enter-to, .fade-leave
        opacity: 1
    .fade-enter-active, .fade-leave-active
        transition: opacity .3s

    @mixin button
        display: flex
        align-items: center
        justify-content: center
        position: absolute
        width: 50px
        height: 50px
        top: 25px
        right: 25px
        color: red
        box-sizing: border-box
    .responsive
        &__button
            @include button
            background: #fff
            display: none
            @media (max-width: 768px)
                display: flex
        &__menu
            position: absolute
            background: #ffffffd4
            width: 100%
            height: auto
            top: 0
            left: 0
            display: flex
            justify-content: center
            padding: 50px 0
        &__close
            @include button
    img
        width: 35px
    .menu
        &__item
            padding-bottom: 20px
        &__link
            font-size: 1.5rem
            line-height: 20px
            font-weight: 700
            color: #154865
    .submenu__list
        .menu__item
            padding: 5px 0 5px 20px
        .menu__link
            font-size: 1.3rem
</style>
