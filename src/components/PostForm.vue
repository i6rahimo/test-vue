<template >
    <div class="post" v-for="post in posts">
    <div class=""><strong>Название:</strong>{{post.title}}</div>
    <div class=""><strong>Описание:</strong>{{post.body}}</div>
  </div>
</template>
<script>
export default {
    
}
</script>
<style scoped>
    .post {
  padding: 15px;
  border: 2px solid teal;
  margin-top: 15px;
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  flex-direction: column;
}
</style>