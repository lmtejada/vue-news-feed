<template>
  <div id="app">
    <h1 class="title">SproutLoud News!</h1>
    <div class="well">
      <!-- Add your news feed here -->
    </div>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style lang="scss">
* {
  box-sizing: border-box;
}

html,
body {
  background-color: #00955f;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: #2c3e50;
  margin-top: 60px;
  margin-bottom: 60px;
}

.title {
  color: #FFF;
}

.well {
  max-width: 800px;
  border-radius: 5px;
  background-color: #FFF;
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
    background-color: #BBB;
  }

  &:active {
    background-color: #AAA;
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
  border: 1px solid #BBB;
}

.text-muted {
  opacity: 0.75;
}
</style>
