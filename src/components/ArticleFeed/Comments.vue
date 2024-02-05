<script setup>
  import { ref } from 'vue';
  import CommentSingle from './CommentSingle.vue';

  const comments = ref([
    { name: 'Matt Adams', comment: 'Molestias ultricies, ante quam urna ut volutpat, egestas dolor dui, nec hac ultrices nulla non netus.', time: new Date() },
  ]);

  let commentName = ref('');
  let commentEmail = ref('');
  let commentText = ref('');

  const addComment = () => {
    const name = commentName.value;
    const email = commentEmail.value;
    const text = commentText.value;

    if (name && text) {
      comments.value.push({
        name,
        email,
        comment: text,
        time: new Date(),
      });
      // Clear the form after adding the comment
      commentName.value = '';
      commentEmail.value = '';
      commentText.value = '';
    }
  };
</script>

<template>
  <div>
    <h1>Comments</h1>
    <CommentSingle v-for="(comment, index) in comments" :key="index" :name="comment.name" :comment="comment.comment" :time="comment.time" />
    
    <div class="add-a-comment">
      <h1>Add a comment</h1>
      <form @submit.prevent="addComment">
        <input type="text" placeholder="Name" v-model="commentName" />
        <input type="email" placeholder="Email" v-model="commentEmail" />
        <textarea placeholder="Your Comment" v-model="commentText"></textarea>
        <button type="submit">Submit Comment</button>
      </form>
    </div>
  </div>
</template>
