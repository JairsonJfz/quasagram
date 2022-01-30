<template>
  <q-page class="constrain q-pa-md">

    <div class="row q-col-gutter-lg">
    </div>
    <div class="col-12 col-sm-8">
      </div>
   <q-card
    v-for="post in posts"
      :key="post.id"
      class="card-post q-mb-md"
      bordered
      flat 
   >
      <q-item>
        <q-item-section avatar>
          <q-avatar>
            <img src="https://cdn.quasar.dev/img/boy-avatar.png">
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-bold">Quasargram </q-item-label>
          <q-item-label caption>
              {{ post.location }}
          </q-item-label>
        </q-item-section>
      </q-item>
      <q-separator />
       <q-img
        :src="post.imageUrl"
      />

       <q-card-section>
        <div>{{ post.caption }}</div>
        <div class="text-caption text-grey">{{ post.date }}</div>
      </q-card-section>
    </q-card>
    <div class="col-4" large-screen-onl>
            <q-item class="fixed">
        <q-item-section avatar>
          <q-avatar size="48px">
            <img src="https://cdn.quasar.dev/img/boy-avatar.png">
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-bold">JairsonJfz </q-item-label>
          <q-item-label caption>
              JairsonJfz
          </q-item-label>
        </q-item-section>
      </q-item>
    </div>
  </q-page>
</template>

<script>
import { date } from 'quasar'

export default {
  name: 'PageHome',
  data() {
    return {
      posts: [
        {
          id: 1,
          caption: 'Torre de Lbidondas',
          date:1591776655504,
          location: 'choupal, Mozambique',
          imageUrl: 'https://cdn.quasar.dev/img/parallax2.jpg'
        },
        {
          id: 2,
          caption: 'Torre de Lbidondas',
          date:1591776655504,
          location: 'choupal, Mozambique',
          imageUrl: 'https://cdn.quasar.dev/img/parallax2.jpg'
        },
        {
          id: 3,
          caption: 'Torre de Lbidondas',
          date:1591776655504,
          location: 'choupal, Mozambique',
          imageUrl: 'https://cdn.quasar.dev/img/parallax2.jpg'
        },
        {
          id: 4,
          caption: 'Torre de Lbidondas',
          date:1591776655504,
          location: 'choupal, Mozambique',
          imageUrl: 'https://cdn.quasar.dev/img/parallax2.jpg'
        }
      ] 
    }
  },
  filters: {
    niceDate(value) {
      return date.formatDate(value, 'YYYY-MM-DDTHH:mm:ss.SSSZ')
    }
  }
} 
</script>


<style lang="sass">
  .card-post
    .q-img
    min-heght: 200px 

</style>
