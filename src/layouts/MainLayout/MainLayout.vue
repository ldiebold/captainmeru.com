<script setup lang="ts">
import { mdiPhone } from '@quasar/extras/mdi-v7'
</script>

<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="shadow-1">
      <q-toolbar>
        <q-toolbar-title class="text-weight-light">
          CaptainMeru.Com
        </q-toolbar-title>
        <q-space />
        <div>
          Call Captain Meru Today!
        </div>
        <div class="q-mx-md">
          -
        </div>
        <q-btn
          type="a"
          href="tel:6711473"
          label="6711 473"
          flat
          :icon="mdiPhone"
        />
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>
