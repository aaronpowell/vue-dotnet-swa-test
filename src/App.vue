<template>
  <div>{{ value }}</div>
</template>

<script>
import axios from "axios";
export default {
  name: "App",
  async mounted() {
    const res = await axios.get("/api/GetMessage?name=Aaron");
    this.value = res.data;
  },
  data() {
    return {
      value: "Waiting for server response",
    };
  },
};
</script>
