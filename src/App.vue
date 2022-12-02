
<template>
  <div class="app">
    <post-list/>
  </div>
</template>

<script>
    import PostForm from "@/components/PostForm";
    import PostList from "@/components/PostList";

    export default { 
      components: {
        PostList, PostForm
      },
      data() {
        return {
          posts: [
            {id: 1, title: 'JavaScript', body: 'Описание поста'},
            {id: 2, title: 'JavaScript', body: 'Описание поста 2'},
            {id: 3, title: 'JavaScript', body: 'Описание поста 3'},
          ],
          title: '',
          body: '',
        }
      },
      methods: {
        createPost() {
          const newPost = {
            id: Date.now(),
            title: this.title,
            body: this.body, 
          }
          this.posts.push(newPost),
          this.title = '',
          this.body = ''
        }
      }
    }
</script>

<style scoped>
.input {
  width: 100%;
  border: 1px solid teal;
  padding: 10px 15px;
  margin-top: 15px;
}
.dialog {
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  display: flex;
}
.dialog__content {
  margin: auto;
  background: white;
  border-radius: 12px;
  min-height: 50px;
  min-width: 300px;
  padding: 20px;
}
form {
  display: flex;
  flex-direction: column;
}.navbar {
  height: 50px;
  background-color: lightgray;
  box-shadow: 2px 2px 4px gray;
  display: flex;
  align-items: center;
  padding: 0 15px;
}
.btn {
  padding: 10px 15px;
  background: none;
  color: teal;
  border: 1px solid teal;
}
.navbar__btns {
  margin-left: auto;
}


.post__btns {
  display: flex;
}
.user-list-item {
  display: inline-block;
  margin-right: 10px;
}
.user-list-enter-active,
.user-list-leave-active {
  transition: all 0.4s ease;
}
.user-list-enter-from,
.user-list-leave-to {
  opacity: 0;
  transform: translateX(130px);
}
.user-list-move {
  transition: transform 0.4s ease;
}
</style>
