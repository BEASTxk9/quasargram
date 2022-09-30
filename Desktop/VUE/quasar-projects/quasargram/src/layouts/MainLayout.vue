<template>
  <q-layout view="lHh Lpr lFf">
    <!-- header -->
    <q-header class="bg-white text-grey-10" bordered>
      <q-toolbar class="constrain">

        <!-- camera btn -->
        <q-btn to="/camera" class="large-screen-only q-mr-sm" flat round icon="eva-camera-outline" size="18px" dense />

        <q-separator
        class="large-screen-only"
        vertical
        spaced
         />

        <!-- logo -->
        <q-toolbar-title class="text-grand-hotel text-bold">
          Quasargram
        </q-toolbar-title>

        <!-- home btn -->
        <q-btn to="/" class="large-screen-only" flat round icon="eva-home-outline" size="18px" dense />

      </q-toolbar>



    </q-header>

    <!-- main -->
    <q-page-container class="bg-grey-1">
      <router-view />
    </q-page-container>

    <!-- footer -->
    <q-footer class="small-screen-only bg-white text-grey-10" bordered>

      <q-tabs active-color="primary" indicator-color="transparent">
        <q-route-tab to="/" icon="eva-home-outline" />
        <q-route-tab to="/camera" icon="eva-camera-outline" />
      </q-tabs>

    </q-footer>


  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  data() {
    return {

    }
  },
})
</script>

<style lang="sass">
.q-toolbar
 @media (min-width: $breakpoint-sm-min)
  height: 60px

.q-toolbar__title
 font-size: 30px
 @media (max-width: $breakpoint-xs-max)
  text-align: center

.q-footer
 .q-tab__icon
  font-size: 30px
</style>
