<template>
  <p>
    <small>
      <template v-if="post.author">
        Diterbitkan {{ post.date }} oleh
        <template v-for="(author, i) in post.author">
          <span v-if="i && i === post.author.length - 1"> dan </span>
          <span v-else-if="i > 0">, </span>

          <g-image v-if="author.avatar" class="author-image" :alt="author.title"  :src="author.avatar" />

          <g-link :to="author.path" :key="author.id">{{ author.title }}</g-link>

        </template>
      </template>
    </small>
  </p>
</template>

<script>
export default {
  props: {
    post: { type: Object, required: true }
  }
}
</script>

<style>
.author-image {
  width: 30px;
  border-radius: 99px;
  vertical-align: middle;
  margin: 0 6px;
}
</style>