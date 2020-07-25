<template>
  <div class="row">
    <div class="col-sm-3">
      <div class="form-group">
        <label for="esquerda">Esquerda </label>
        <select
          v-bind:multiple="true"
          class="form-control"
          name="esquerda"
          id="esquerda"
          v-model="modelo.direita"
        >
          <option
            v-for="(esq, index) in esquerda"
            v-bind:key="index"
            v-bind:value="index"
          >
            {{ esq }}
          </option>
        </select>
      </div>
    </div>
    <div class="col-sm-3 mt-5">
      <button
        type="button"
        class="btn btn-outline-info"
        v-on:click="enviarEsquerda()"
      >
        <span class="fa fa-chevron-left"></span>
      </button>
      <button
        type="button"
        class="btn btn-outline-info"
        v-on:click="enviarDireita()"
      >
        <span class="fa fa-chevron-right"></span>
      </button>
    </div>
    <div class="col-sm-3">
      <div class="form-group">
        <label for="direita">Direita </label>
        <select
          v-bind:multiple="true"
          class="form-control"
          name="direita"
          id="direita"
          v-model="modelo.esquerda"
        >
          <option
            v-for="(dir, index) in direita"
            v-bind:key="index"
            v-bind:value="index"
          >
            {{ dir }}
          </option>
        </select>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CustomList",
  data: () => {
    return {
      esquerda: ["20", "30", "40", "50"],
      direita: [],
      modelo: {
        esquerda: [],
        direita: [],
      },
    };
  },
  methods: {
    enviarDireita() {
      // console.log(this.modelo.direita[0]);
      const valor = this.modelo.direita[0];
      console.log(this.esquerda[valor]);
      this.direita.push(this.esquerda[valor]);

      this.$delete(this.esquerda, valor);
    },
    enviarEsquerda() {
      // console.log(this.modelo.esquerda[0]);
      const valor = this.modelo.esquerda[0];
      this.esquerda.push(this.direita[valor]);

      this.$delete(this.direita, valor);
    },
  },
};
</script>
