<template>
  <div id="containerLogin" class="q-pa-md q-gutter-y-md">
    <p class="text-h6">Login:</p>
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
          <q-btn color="purple">Login</q-btn>
          <q-btn
            id="btnNovaConta"
            flat style="color: #a603b4"
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

</script>

<style scoped>
#containerLogin {
  padding-top: 60px;
}
p {
  color: rgb(165, 53, 165);
  text-align: center;
  font-family: 'Verdana';
  font-weight: bold;
  padding-bottom: 10px;
}
</style>
