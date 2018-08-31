<template>
  <div class="post">
    <article class="post-item">
        <div class="post-header">
            <h1 v-html="post.title"></h1>
        </div>
        <div class="post-publisher">
            <div class="post-author" v-html="post.author"></div>
        </div>
        <div class="post-content" v-html="post.content"></div>
    </article>
  </div>
</template>

<script>
    export default {
        name: 'post',

        data() {
            return {
                post: {}
            }
        },

        created() {
            this.getPost()
        },

        methods: {
            getPost() {
                this.$http.get(`/content/${this.$route.params.slug}`).then((response) => {
                    this.post = response.data;
                });
            }
        }
    }
</script>

<style>
    .post-publisher {
        margin-bottom: 25px;
    }
</style>
