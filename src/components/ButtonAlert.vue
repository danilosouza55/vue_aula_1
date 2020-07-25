<template>
  <div>
    <button type="button" class="btn btn-danger" v-on:click="clickAlert()">
      Alerta
    </button>
  </div>
</template>

<script>
export default {
  name: "ButtonAlert",
  methods: {
    clickAlert() {
      alert("oi Imundo!!!");
    },
  },
};
</script>
