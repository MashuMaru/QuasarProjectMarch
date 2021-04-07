<template>
  <q-layout view="hHh Lpr fFf">
    <!-- Be sure to play with the Layout demo on docs -->

    <!-- (Optional) The Header -->
    <q-header elevated class="row justify-center">
      <q-toolbar class="col">
        <q-toolbar-title>
          Quasar Test App
        </q-toolbar-title>
      </q-toolbar>

      <q-tabs>
        <q-route-tab v-bind:to="{ name: 'home', path: '', }" label="Home" />
        <q-route-tab
          v-bind:to="{ name: 'profile', params: { id: 1 } }"
          replace
          label="Walter"
        />
        <q-route-tab
          v-bind:to="{ name: 'profile', params: { id: 2 } }"
          replace
          label="Jesse"
        />
        <q-route-tab
          v-bind:to="{ name: 'profile', params: { id: 'random' } }"
          replace
          label="Random"
        />
      </q-tabs>
    </q-header>

    <q-page-container>
      <!-- This is where pages get injected -->
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  // name: 'LayoutName',

  data() {
    return {
      leftDrawer: true
    };
  }
};
</script>
