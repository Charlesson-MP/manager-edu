<template>
  <q-page padding class="flex flex-center">
    <q-form id="formulario" class="row justify-center" @submit.prevent="">
      <p id="tituloFormulario" class="text-h5">Tela de cadastro</p>
      <div class="col-md-7 col-sm-6 col-xs-6 q-gutter-y-md">
        <q-input
          label="Usuário"
          color="purple"
          bg-color="white"
          filled
          v-model="usuario"
        />

        <q-input bg-color="white" color="purple" v-model="senha" label="Senha" filled :type="isPwd ? 'password' : 'text'" hint="Password with toggle">
          <template v-slot:append>
            <q-icon
              :name="isPwd ? 'visibility_off' : 'visibility'"
              class="cursor-pointer"
              @click="isPwd = !isPwd"
            />
          </template>
        </q-input>

        <q-btn
          label="Cadastrar"
          style="color: #8019e0"
          class="full-width"
          outline
          size="lg"
          @click="cadastrar"
          to="/"
        />
      </div>
    </q-form>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const usuario = ref('')
const senha = ref('')
const isPwd = ref(true)

function cadastrar () {
  alert('Ola')
}
</script>

<style scoped>
#formulario {
  padding: 30px 0px 30px 0px;
  background-color: #d1c6eb;
  border-radius: 20px;
}

#tituloFormulario {
  color: rgb(128, 25, 224);
  text-align: center;
  font-family: 'Verdana';
  font-weight: bold;
  padding-bottom: 10px;
}

</style>
