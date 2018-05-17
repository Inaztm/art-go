<template lang="pug">
  section
    .space-bottom
      titles(
        bigTitle="Коллекции",
        smallTitle="32000 ПРОСМОТРОВ"
      )

    .space-top
      section.row(
        v-for="collection in collections"
      )
        .col-xs-12.col-sm-6.col-lg-4(v-for="i in 8")
          a.collection(href="#")
            .collection__cards
              template(
                v-for="collAttach in collection.attach"
              )
                .collection__card(
                  :style="{ backgroundImage: 'url(' + collAttach.src + ')' }"
                )

            .collection__title {{ collection.name }}

</template>

<script>
import Behance from 'node-behance-api'

import titles from '~/components/Titles.vue'

export default {
  components: {
    titles
  },
  data () {
    return {
      colls: [],
      collections: [
        {
          id: 1,
          name: 'Web design',
          attach: [
            {
              id: 1,
              src: '/images/cover.jpg'
            },
            {
              id: 2,
              src: '/images/cover.jpg'
            },
            {
              id: 3,
              src: '/images/cover.jpg'
            }
          ]
        }
      ]
    }
  },
  methods: {
    getCollections: () => {
      const clientId = '80lpL2RmUr4xOuJAnioopotqzDO4EesJ'

      var behance = new Behance({"client_id": clientId})

      Behance.initOptions();
      
      behance.get({
          api: Behance.APIS.GET_USER,
          params: { //or simply behance.get('user',
              user:'deepakmshrma'

          }
      }, function (error, result) {
          if (error)
              console.log(error)
          else
              console.log(result)
      });
    }
  },
  mounted () {
    this.getCollections()
  }
}
</script>

