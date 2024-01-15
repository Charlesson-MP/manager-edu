<template>
  <div id="containerLogin" class="q-pa-md q-gutter-y-md">
    <p class="text-h6">Login</p>
      <div id="login" class="q-gutter-y-md column" style="max-width: 300px">
        <q-input bg-color="white" v-model="usuario" color="purple" filled label="Usuário" />
      </div>
      <div id="senha" class="q-gutter-y-md column" style="max-width: 300px">
        <q-input bg-color="white" color="purple" v-model="senha" label="Senha" filled :type="isPwd ? 'password' : 'text'" hint="Password with toggle">
          <template v-slot:append>
            <q-icon
              :name="isPwd ? 'visibility_off' : 'visibility'"
              class="cursor-pointer"
              @click="isPwd = !isPwd"
            />
          </template>
        </q-input>
      </div>
      <div id="inscSubmit" class="q-gutter-x-lg">
          <q-btn
            style="background-color: #8019e0; color: white"
            @click="logar"
          >Login</q-btn>
          <q-btn
            id="btnNovaConta"
            flat style="color: #8019e0"
            label="Criar conta"
            to="register"
          />
        </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const usuario = ref('')
const senha = ref('')
const isPwd = ref(false)

function logar () {
  alert('Ola')
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
</style>
