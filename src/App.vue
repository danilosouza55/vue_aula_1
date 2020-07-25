<template>
  <div id="app">
    <div class="container">
      <h3>Clique no botão a baixo</h3>
      <ButtonAlert btnTitle="Nome do botão" message="Web dev" />
      <CustomList />
    </div>
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.css";
import "font-awesome/css/font-awesome.css";
import ButtonAlert from "./components/ButtonAlert";
import CustomList from "./components/CustomList";

export default {
  name: "App",
  components: {
    ButtonAlert,
    CustomList,
  },
};
</script>
