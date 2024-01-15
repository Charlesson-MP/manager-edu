<template>
  <div id="containerLogin" class="q-pa-md q-gutter-y-md text-center">
    <p class="text-h6" >Menu</p>
    <q-btn padding="10px 110px" id="opcaoInicio"  @click="goAlunos" >Início</q-btn>
    <q-btn padding="10px 105px" id="opcaoAlunos" @click="goAlunos">Alunos</q-btn>
    <q-btn padding="10px 99px" id="opcaoModulos" @click="goModulos">Módulos</q-btn>
  </div>
</template>

<script setup>
function goAlunos () {
  alert('Go alunos')
}
function goModulos () {
  alert('Go módulos')
}
</script>

<style scoped>
#containerLogin {
  padding-top: 15px;
}
p {
  color: white;
  text-align: center;
  font-family: 'Verdana';
  font-weight: bold;
  padding: 10px;
  background-color: rgb(128, 25, 224);
  border-radius: 10px;
}
#opcaoAlunos {
  background-color: rgb(240, 235, 245);
  text-align: center;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  font-size: larger;
  color: rgb(101, 10, 187);
}

#opcaoModulos {
  background-color: rgb(240, 235, 245);
  text-align: center;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  font-size: larger;
  color: rgb(101, 10, 187);
}
#opcaoInicio {
  background-color: rgb(240, 235, 245);
  text-align: center;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  font-size: larger;
  color: rgb(101, 10, 187);
}
</style>
