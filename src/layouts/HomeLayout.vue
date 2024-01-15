<script setup>
import { ref } from 'vue'
import SideBarHomePage from 'src/components/SideBarHomePage.vue'

const rightDrawerOpen = ref(false)

function toggleRightDrawer () {
  rightDrawerOpen.value = !rightDrawerOpen.value
}

</script>

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

        <q-btn label=" MENU" dense flat round icon="menu" @click="toggleRightDrawer" />
      </q-toolbar>
    </q-header>

    <q-drawer
      :show-if-above="false"
      :breakpoint="700"
      v-model="rightDrawerOpen"
      side="right"
      elevated>
      <!-- drawer content -->
      <SideBarHomePage/>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<style>
.q-header {
  background-color: rgb(92, 2, 177);
}

.q-drawer {
  background-color: rgb(210, 202, 230);
}
</style>
