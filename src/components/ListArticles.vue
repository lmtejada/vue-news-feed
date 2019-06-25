<template>
  <div>
    <div v-for="(article, index) in articles" :key="index">
      <h2>{{ article.title }}</h2>
      <p>{{ article.body }}</p>
      <post-comment @addComent="newComment" :article="index"></post-comment>
      <div class="comments">
        <h3>Comments</h3>
        <list-comments :comments="article.comments"></list-comments>
      </div>
    </div>
  </div>
</template>
<script>
import axios from "axios";
import PostComment from "./PostComment.vue";
import ListComments from "./ListComments.vue";

export default {
  data() {
    return {
      articles: []
    };
  },
  components: {
    PostComment,
    ListComments
  },
  methods: {
    newComment(data) {
      const uuid = require('uuid/v4');
      this.articles[data.article]["comments"].push({
        comment_id: uuid(),
        date: new Date(),
        author: "Laura Tejada",
        body: data.text
      });
    }
  },
  created() {
    axios
      .get("data/articles.json")
      .then(response => {
        this.articles = response.data;
      })
      .catch(error => {
        alert(error);
      });
  }
};
</script>
<style>
p {
  line-height: 2rem;
  color: rgb(56, 56, 56);
  font-weight: 300;
}

h2 {
  margin-top: 30px;
}
.comments {
  width: 80%;
}
</style>

