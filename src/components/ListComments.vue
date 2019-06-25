<template>
    <div class="comments">
        <div v-for="(comment, index) in comments" :key="index" class="post">
            <h4>{{ comment.author }}</h4>
            <p>{{ comment.body }}</p>
        </div>
    </div>
</template>
<script>
export default {
    props: ['comments']
}
</script>

<style scoped>
.post {
    background: rgba(231, 231, 231, 0.24);
    font-size: 0.8rem;
    padding: 20px;
    margin-bottom: 5px;
    border-radius: 8px;
}

h4 { margin: 5px 0px !important;}
p {
    line-height: 12px;
}
</style>


