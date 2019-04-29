<template>
    <div id="app">
        <img src="./assets/logo.png" style="width: 100px;">
        <h1>Testing props</h1>
        <div>
            <Parent :client="client"/>
        </div>
        <div class="box">
            <strong>App.vue</strong>
            <pre v-html="client"></pre>
        </div>
    </div>
</template>

<script>
  import Parent from "./components/Parent";

  export default {
    name: "App",
    data () {
      return {
        client: {
          name: "",
          age: ""
        }
      };
    },
    components: {
      Parent
    }
  };
</script>

<style>
    .box {
        padding: 10px;
        border: 1px solid #DDD;
        width: 200px;
        margin-top: 15px;
    }
</style>
