<template>
  <q-page class="constrain q-pa-md">

<div class="row q-col-gutter-lg">

  <!-- left posts -->
  <div class="col-12 col-sm-8">

 <q-card
    v-for="post in posts"
    :key="post.id"
    class="card-post q-mb-md" flat bordered>
         <!-- user data header -->
      <q-item>

        <q-item-section avatar>
          <q-avatar>
            <img src="https://cdn.quasar.dev/img/boy-avatar.png">
          </q-avatar>
        </q-item-section>

        <q-item-section>

          <q-item-label class="text-bold">
            BEASTxk9
          </q-item-label>

          <q-item-label caption>
            {{ post.location }}
          </q-item-label>

        </q-item-section>
      </q-item>

      <q-separator />

<!-- user post data -->
      <q-img
        :src="post.imageUrl"
      />

      <q-card-section>
        <div>{{ post.caption }}</div>
        <div class="text-caption text-grey">
          {{ niceDate(post.date) }}
        </div>
      </q-card-section>

    </q-card>

  </div>

  <!-- right profile -->
  <div class="col-4 large-screen-only">

    <q-item class="fixed">

<q-item-section avatar>
  <q-avatar size="48px">
    <img src="https://cdn.quasar.dev/img/boy-avatar.png">
  </q-avatar>
</q-item-section>

<q-item-section>

  <q-item-label class="text-bold">
    BEASTxk9
  </q-item-label>

  <q-item-label caption>
    Shane Stevens
  </q-item-label>

</q-item-section>
</q-item>

  </div>

</div>




  </q-page>
</template>

<script>
import { defineComponent } from 'vue';
import { date } from 'quasar';

export default defineComponent({
  name: 'PageHome',
  data(){
    return {
      posts: [
        {
          id: '1',
          caption: 'Golden Gate Bridge',
          date: 1664521178835,
          location: 'Cape Town, Western Cape, South Africa',
          imageUrl: 'https://cdn.quasar.dev/img/parallax2.jpg'
        },
        {
          id: '2',
          caption: 'Golden Gate Bridge',
          date: 1664521178835,
          location: 'Cape Town, Western Cape, South Africa',
          imageUrl: 'https://cdn.quasar.dev/img/parallax2.jpg'
        },
        {
          id: '3',
          caption: 'Golden Gate Bridge',
          date: 1664521178835,
          location: 'Cape Town, Western Cape, South Africa',
          imageUrl: 'https://cdn.quasar.dev/img/parallax2.jpg'
        },
        {
          id: '4',
          caption: 'Golden Gate Bridge',
          date: 1664521178835,
          location: 'Cape Town, Western Cape, South Africa',
          imageUrl: 'https://cdn.quasar.dev/img/parallax2.jpg'
        },
      ]
    }
  },
  methods: {
    niceDate(value){
return date.formatDate(value, 'MMMM D h:mmA')
    }
  }
})
</script>

<style lang="sass">
.card-post
 .q-img
  min-height: 200px
</style>
