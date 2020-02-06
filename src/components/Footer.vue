<template lang="pug">
    footer.footer
        .footer__wrap.wrap
            ul.footer__list
                li.footer__item
                    | P +64 9555 555
                li.footer__item
                    | F +64 9555 555
                li.footer__item
                    a.footer__link(href="#") E info@email.com
                li.footer__title
                    | Address
                li.footer__item
                    a.footer__link(href="#") http://www.lipsum.com/feed/html
            ul.footer__list
                li.footer__title Services
                each val in ['Commercial', 'Distribution', 'Gas', 'Generation', 'Industrial', 'Telecomms', 'Transmission', Water]
                    li
                        a.footer__link(href="#")= val
            ul.footer__list
                li.footer__title Markets
                each val in ['Commercial', 'Industrial', 'Infrastructure', 'Resources', 'Utitlities']
                    li
                        a.footer__link(href="#")= val
            ul.footer__list
                li.footer__title HSEQ
                each val in ['Health', 'Safety', 'Environment', 'Quality']
                    li
                        a.footer__link(href="#")= val
            ul.footer__list
                li.footer__title About
                each val in ['History', 'Structure', 'People', 'CSR', 'Locations', 'PPV']
                    li
                        a.footer__link(href="#")= val
            ul.footer__list
                li.footer__title Careers
                each val in ['Who we are', 'Benefits', 'Programmes', 'Our People', 'Roles', 'Vacancies']
                    li
                        a.footer__link(href="#")= val
</template>

<style lang="sass" scoped>
    .footer
        background: #e87a77
        &__wrap
            max-width: 968px
            display: grid
            grid:
                template-columns: 1fr repeat(5, auto)
                column-gap: 80px
            padding:
                top: 50px
                bottom: 222px
            font-size: 12px
            line-height: 24px
            font-family: 'Droid Serif Bold', arial
        &__list
            list-style: none
        &__title
            font-weight: 600
            font-size: 1rem
        &__list:first-child .footer__title
            padding-top: 40px
        &__link
            color: #fff
            text-decoration: none
            font-size: .9rem
            transition: color .3s
            &:hover
                color: #942b28

    @media (max-width: 1024px)
        .footer__wrap
            grid-column-gap: 50px

    @media (max-width: 960px)
        .footer__wrap
            grid:
                template-columns: repeat(3, auto)
                gap: 40px
            padding-bottom: 50px

    @media (max-width: 768px)
        .footer__wrap
            grid:
                template-columns: repeat(2, auto)
                gap: 10px
            padding: 20px 15px

    @media (max-width: 320px)
        .footer
            &__wrap
                grid-template-columns: auto
            &__list
                text-align: center

</style>
