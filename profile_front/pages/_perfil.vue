<template>
  <div class="page-holder bg-gray-100 mt-5">
      <b-container class="bv-example-row">
        <b-row>
          <b-col cols="12" class="d-flex justify-content-center">
            <b-avatar v-bind:src=foto size="12rem"></b-avatar>
          </b-col>
          <b-col cols="" class="bg-info  mt-2">
            <div class="text-center mb-3 title text-secundario font-weight-bold">
                <span>@</span>{{pagina}}
            </div>
            <div class="text-center mb-3">
              <span>{{ frase }}</span>
            </div>
            <div class="text-center mb-3">
              <b-icon icon="geo-alt-fill" scale="1.5"></b-icon> {{ localizacao }}  
            </div>
            <div class="text-center mb-3">
              <span>{{ frase }}</span>
            </div>
          </b-col>
        </b-row>
        <b-row >
          <b-col class="text-center">           
            <span class="font-weight-bold">Seguidores: </span>{{seguidores}}
          </b-col>
          <b-col class="text-center">
            <span class="font-weight-bold">Seguindo: </span>{{seguindo}}
          </b-col>
        </b-row>
      </b-container>
  </div>
</template>

<script>
export default {
  name: 'PerfilPage',
  
  data() {
    return {
      nome: "Rodrigo Faro",
      frase: "Só quem ama não pisa. Cuida, valoriza. (Banda Revelação)",
      localizacao: "Brasil, São Paulo",
      foto: "data:image/jpeg;base64,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",
      seguidores: 450,
      seguindo: 20
    }
  },
  computed:{
    pagina(){
      return this.nome.replace(" ", "").toLocaleLowerCase();
    }
  }
}
</script>

