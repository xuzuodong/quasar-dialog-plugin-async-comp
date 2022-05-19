<script setup lang="ts">
import { Dialog } from 'quasar'
import DialogVue from './Dialog.vue'

function regularDialog() {
  Dialog.create({
    component: () => import('./Dialog.vue'),
  })
}

function asyncDialog() {
  Dialog.create({
    component: DialogVue,
  })
}
</script>

<template>
  <main font-sans p="x-4 y-10" text="center gray-700 dark:gray-200">
    <div mb-10>
      <button @click="regularDialog">
        open regular dialog
      </button>
    </div>

    <div>
      <button @click="asyncDialog">
        open async dialog
      </button>
    </div>
  </main>
</template>
