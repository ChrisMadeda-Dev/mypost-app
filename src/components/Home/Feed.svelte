<script>
	let showAddContent = false;
	import FeedCont from './FeedCont.svelte';
	import FeedSideNav from './FeedSideNav.svelte';
	import { feedstore } from '../../stores/store';
</script>

<div class="feed">
	<header>
		<h1>MYPOST</h1>
	</header>
	{#each $feedstore as feedContent}
		<FeedCont {feedContent} />
	{/each}
	
</div>

<style>
	.feed {
		flex: 0 0 55%;
		height: 99%;
		gap: 12px;
		padding: 20px 0px;
		background-color:#1b1b1b;
		display: flex;
		flex-direction: column;
		justify-content: flex-start;
		align-items: center;
		overflow-y: scroll;
		overflow-x: hidden;
		color: white;
	}

	.feed > header {
		width: 100%;
		flex: 0 0 20vh;
		background-color: '';
		display: flex;
		justify-content: center;
		align-items: center;
	}
</style>
