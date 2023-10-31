<script>
	function toAddPost() {
		window.location.href = '/AddPost';
	}
</script>

<div class="feed-side-nav">
	<div class="top">
		<span>HI Chris</span>
	</div>
	<div class="center">
		<button>Home</button>
		<button><a href="/profile">Profile</a></button>
		<button>Search</button>
		<button>Settings</button>
	</div>
	<div class="bottom">
		<button on:click={toAddPost}>Add Post</button>
	</div>
</div>

<style>
	.feed-side-nav {
		flex: 0 0 13%;
		height: 99%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		border-right: 1px solid #353839;
		background-color: #1b1b1b;
		color: white;
	}

	button {
		outline: none;
		border: none;
		border-radius: 5px;
		width: 80%;
		min-width: 80%;
		height: 40px;
		background-color: #353839;
		color: white;
	}

	.top {
		flex: 0 0 20%;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.center {
		width: 100%;
		flex: 0 0 70%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 9px;
	}

	.bottom {
		width: 100%;
		flex: 0 0 10%;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.bottom > button {
		background-color: brown;
		color: white;
		width: 80%;
	}
</style>
