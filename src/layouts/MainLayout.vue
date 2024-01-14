<template>
  <q-layout view="hhr lpR fFr">

    <q-header elevated class="text-white">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <img style="width: 60px;" src="../assets/manager-edu-logo-pequeno.svg">
          </q-avatar>
          Manager Edu
        </q-toolbar-title>

        <q-btn label=" LOGIN" dense flat round icon="login" @click="toggleRightDrawer" />
      </q-toolbar>
    </q-header>

    <q-drawer
      :show-if-above="false"
      :breakpoint="700"
      v-model="rightDrawerOpen"
      side="right"
      elevated>
      <!-- drawer content -->
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    const rightDrawerOpen = ref(false)

    return {
      rightDrawerOpen,
      toggleRightDrawer () {
        rightDrawerOpen.value = !rightDrawerOpen.value
      }
    }
  }
}
</script>

<style>
.q-header {
  background-color: rgb(104, 10, 122);
}
</style>
