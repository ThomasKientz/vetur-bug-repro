<template>
  <div id="app">
    {{ foo }}
    <img alt="Vue logo" src="./assets/logo.png" @click="test" />
    <vue-flux />
  </div>
</template>

<script>
import { VueFlux } from "vue-flux";

export default {
  name: "App",

  components: {
    VueFlux,
  },

  data() {
    return {
      foo: "bar",
    };
  },

  created() {
    this.test();
  },

  computed: {
    bar() {
      return this.foo;
    },
  },

  methods: {
    test() {
      console.log(this.foo);
    },
  },
};
</script>
