<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-white text-grey-10">
      <q-toolbar class="contrain" >
        <q-btn
          to="/camera"
          class="large-screem-only q-mr-sm"
          icon="eva-camera-outline"
          flat
          round
          size="18px"
          dense 
          />
          <q-separator
            vertical
            spaced
          />  
        <q-toolbar-title class="text-grand__hotel">
          Instagram 
        </q-toolbar-title>
          <q-btn
          to="/"
          icon="eva-home-outline"
          flat
          round
          size="18px"
          dense 
          />
      </q-toolbar>
    </q-header>

    <q-footer class="bg-white"
      bordered
    >
            <q-tabs class="text-grey-10"
              active-color="primary"
              indicator-color="transparent"
            >
            <q-route-tab
              to="/"
              icon="eva-home-outline" 
            />
             <q-route-tab
              to="/camera"
              icon="eva-camera-outline" 
            />
          </q-tabs>
      </q-footer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>


import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',

})
</script>

<style lang="sass">
  .q-toolbar__title
    text-align: center
    font-size:30px
  .q-footer
    .q-tab__icon
      font-size: 30px
</style> 