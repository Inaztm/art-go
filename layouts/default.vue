<template lang="pug">
  .big-wrapper
    .banner-image
    main.page
      nav.navigation
        section.space-x.space-top.space-bottom-sm
          nuxt-link.flex.--center-items(:to="{ path: '/' }")
            i.site-inc.--space
            h3 ArtGO portfolio
        
        section.navigation__scroll-flex
          .list
            nuxt-link.list__link(
              :to="{ name: 'collections' }",
              active-class="--active")
              i.mi.mi-AllApps.space-right-sm
              span Коллекции

            nuxt-link.list__link(
              :to="{ name: 'order' }",
              active-class="--active")
              i.mi.mi-Send.space-right-sm
              span Заказать работу

            nuxt-link.list__link(
              :to="{ name: 'about' }",
              active-class="--active")
              i.mi.mi-Accounts.space-right-sm
              span Обо мне

        section.space-y
          .list
            nuxt-link.list__link(
              :to="{ name: 'settings' }",
              active-class="--active")
              i.mi.mi-Settings.space-right-sm
              span Настройки

      section.content
        nuxt
</template>

<style lang="stylus">

  @import '../assets/stylus/main.styl'

</style>
