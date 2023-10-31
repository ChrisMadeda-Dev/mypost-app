<script>
	import { feedstore } from '../../stores/store';
	let post;

	function addPost() {
		if ((post.trim().length >= 2, post)) {
			feedstore.update((curr) => {
				return [...curr, { content: post }];
			});
			console.log(post);
		}

		post=''
	}
</script>

<div class="add-post">
	<div class="top">''</div>
	<div class="center">
		<textarea bind:value={post} />
	</div>
	<div class="bottom">
		<button on:click={addPost}>Add Post</button>
	</div>
</div>

<style>
	.add-post {
		width: 100%;
		height: 100vh;
		background-color: #1b1b1b;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	.center {
		flex: 0 0 70%;
		width: 60%;
		background-color: '';
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	.center > textarea {
		width: 90%;
		height: 100%;
		resize: none;
		outline: none;
		border: none;
		padding: 20px;
		border-radius: 10px;
		background-color: #353839;
		color: white;
		font-size: 18px;
	}

	.bottom {
		flex: 0 0 10%;
		width: 60%;
		display: flex;
		justify-content: center;
		align-items: center;
		margin: 10px;
	}

	.bottom > button {
		width: 90%;
		height: 55px;
		outline: none;
		border: none;
		background-color:brown;
		border-radius: 10px;
		color: whitesmoke;
		font-size: 16px;
	}

	.bottom > button:hover {
		opacity: 0.8;
	}
</style>
