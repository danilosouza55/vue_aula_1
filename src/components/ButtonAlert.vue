<template>
  <div>
    <button type="button" class="btn btn-danger" v-on:click="clickAlert()">
      {{ btnTitle }}
    </button>
  </div>
</template>

<script>
export default {
  name: "ButtonAlert",
  methods: {
    clickAlert() {
      const msg = this.message;
      alert(msg);
    },
  },
  props: ["btnTitle", "message"],
};
</script>
