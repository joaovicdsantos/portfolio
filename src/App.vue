<template>
  <div id="app">
    <Main/>
  </div>
</template>

<script>
import Main from "./layouts/Main";

export default {
  name: "App",
  components: {
    Main,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Lato:wght@400;900&display=swap");

* {
  font-family: "Lato", sans-serif;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  list-style-type: none;
}

a {
  color: #000;
  text-decoration: none;
}

div.divider {
  width: 100%;
  border-top: 1px dashed rgba(255, 255, 255, 0.1);
  margin: 2% 0;
}
</style>
