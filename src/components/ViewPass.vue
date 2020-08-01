<template>
  <div class="form-group">
    <label for="password">Senha</label>
    <div class="input-group">
      <input
        type="password"
        id="password"
        class="form-control"
        aria-describedby="buttons"
        v-model="senha"
        v-if="view===false"
      />
      <input
        type="text"
        id="password"
        class="form-control"
        aria-describedby="buttons"
        v-model="senha"
        v-if="view===true"
      />

      <div class="input-group-append" id="buttons">
        <button type="button" class="btn btn-outline-info" @click="mostrarSenha">
          <span class="fa fa-eye"></span>
        </button>
      </div>
      <small v-if="senha===''">Senha vazia</small>
    </div>
  </div>
</template>

<script>
export default {
  name: "ViewPass",
  data: () => {
    return {
      view: false,
      senha: "",
    };
  },
  methods: {
    mostrarSenha() {
      if (this.view === false) {
        this.view = true;
      } else {
        this.view = false;
      }
    },
  },
};
</script>