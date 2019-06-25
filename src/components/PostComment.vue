<template>
  <div>
    <textarea v-model="text" class="post-text-area" placeholder="Please write a comment about this article..."></textarea>
    <br>
    <button class="btn-submit" @click="newComment">Post</button>
  </div>
</template>
<script>
export default {
  props: ['article'],
  data() {
    return {
      text: ""
    }
  },
  methods: {
    newComment() {
      this.$emit("addComent", {text: this.text, article: this.article});
      this.text = "";
    }
  }
};
</script>
<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css?family=Roboto:100,100i,300,300i,400,400i,500,500i,700,700i,900,900i&display=swap");

div {
  font-family: "Roboto", sans-serif;
}

.post-text-area {
  width: 100%;
  font-size: 18px;
  padding: 10px;
  border-radius: 8px;
  border: none;
  background: #eee;
  margin-right: 10px;
  margin-top: 10px;
  font-family: "Roboto", sans-serif;
}

.btn-submit {
  width: 10%;
  font-size: 18px;
  padding: 10px;
  border-radius: 8px;
  border: none;
  background: #088145;
  color: #fff;
  cursor: pointer;
  margin-top: 5px;

  -webkit-transition: background 0.2s ease-in-out;
  -moz-transition: background 0.2s ease-in-out;
  -o-transition: background 0.2s ease-in-out;
  transition: background 0.2s ease-in-out;

  &:hover {
    background: #04572d;

    -webkit-transition: background 0.2s ease-in-out;
    -moz-transition: background 0.2s ease-in-out;
    -o-transition: background 0.2s ease-in-out;
    transition: background 0.2s ease-in-out;
  }
}
</style>

