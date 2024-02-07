<script setup>
import { ref } from 'vue';
import CommentSingle from './CommentSingle.vue';

const comments = ref([
	{ name: 'Matt Adams', comment: 'Molestias ultricies, ante quam urna ut volutpat, egestas dolor dui, nec hac ultrices nulla non netus.', time: new Date(2024, 1, 5, 23, 20) },
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
		commentName.value = '';
		commentEmail.value = '';
		commentText.value = '';
	}
};
</script>

<template>
	<div class="article-section">
		<h1 class="article-section-title">Comments</h1>
		<CommentSingle v-for="(comment, index) in comments" :key="index" :name="comment.name" :comment="comment.comment" :time="comment.time" />
		<div class="add-a-comment">
			<h1 class="article-section-title">Add a comment</h1>
			<p class="article-text">Molestias ultricies, ante quam urna ut volutpat, egestas dolor dui, nec hac ultrices nulla non netus. Placerat vehicula donec non suscipit egestas, augue vel suspendisse. Et felis venenatis blandit sed est ultrices, adipiscing urna.</p>
			<form @submit.prevent="addComment" class="comment-form">
			<input class="comment-input" type="text" placeholder="Name" v-model="commentName" />
			<input class="comment-input" type="email" placeholder="Email" v-model="commentEmail" />
			<textarea class="comment-input-text" placeholder="Your Comment" v-model="commentText"></textarea>
			<button type="submit" class="submit-comment">Submit</button>
			</form>
		</div>
	</div>
</template>
