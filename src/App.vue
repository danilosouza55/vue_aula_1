<template>
  <div id="app">
    <div class="container">
      <h3>Clique no botão a baixo</h3>
      <ButtonAlert />
    </div>
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.css";
import ButtonAlert from "./components/ButtonAlert";

export default {
  name: "App",
  components: {
    ButtonAlert,
  },
};
</script>
