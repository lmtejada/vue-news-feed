<template>
  <div id="app">
    <div class="container">
      <h1 class="title">SproutLoud News!</h1>
      <div class="well">
        <list-articles></list-articles>
      </div>
    </div>
  </div>
</template>

<script>
import ListArticles from "./components/ListArticles.vue";

export default {
  name: "app",
  components: {
    ListArticles
  }
};
</script>
<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Roboto:100,100i,300,300i,400,400i,500,500i,700,700i,900,900i&display=swap");

* {
  box-sizing: border-box;
}

html,
body {
  background-color: #fff;
  font-family: "Roboto", sans-serif;
}

#app {
  font-family: "Roboto", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: #2c3e50;
  margin-top: 60px;
  margin-bottom: 60px;
  font-weight: 200;
  .container {
    width: 80%;
    text-align: left;
  }
}

.title {
  color: #088145;
  font-weight: 400;
  font-size: 60px;
  margin-top: 0px;
}

.well {
  border-radius: 5px;
  background-color: #fff;
  padding: 0 20px;
}

.button {
  padding: 6px 8px;
  border: 0;
  border-radius: 5px;
  cursor: pointer;

  &:focus {
    outline: 0;
  }

  &:hover {
    background-color: #bbb;
  }

  &:active {
    background-color: #aaa;
  }

  &.button-link {
    background-color: transparent;
    color: #009bb2;

    &:hover {
      cursor: pointer;
      text-decoration: underline;
    }
  }
}

.input {
  width: 100%;
  padding: 6px 8px;
  border-radius: 5px;
  border: 1px solid #bbb;
}

.text-muted {
  opacity: 0.75;
}
</style>
