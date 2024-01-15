<template>
  <div class="row q-gutter-y-sm q-mx-md">
    <q-card id="card" class="col-xs-12 col-sm-12 col-md-12">
      <q-card-section>
        Bem vindo, o objetivo deste software é fornecer um ambiente de gerenciamento de alunos e módulos.
        Aqui você poderá gerenciar seus alunos e módulos com bastante facilidade.
      </q-card-section>
  </q-card>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'CardBoasVindas'
})
</script>

<style>
#card {
  background-color: rgb(210, 202, 230);
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  font-size: larger;
  color: rgb(128, 25, 224);
}
</style>
