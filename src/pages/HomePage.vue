<template>
  <q-page id="pagina" >
      <img
      alt="Manager Edu logo"
      src="../assets/manager-edu-logo.svg"
      style="width: 300px;"
    >
    <CardBoasVindas />
  </q-page>
</template>

<script setup>
import CardBoasVindas from 'src/components/CardBoasVindas.vue'
</script>

<style>
#pagina {
  text-align: center;
  padding-top: 100px;
}
</style>
