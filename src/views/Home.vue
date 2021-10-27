<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld :msg="message" />
    <h1>COMPUTED: {{ computed_message }}</h1>
    <h1>url: {{ url }}</h1>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
  },
  computed: {
    computed_message: function () {
      return process.env.VUE_APP_MESSAGE;
    },
  },
  data() {
    return {
      url: process.env.BASE_URL,
      message: process.env.PUBLIC_PATH,
    };
  },
};
</script>
