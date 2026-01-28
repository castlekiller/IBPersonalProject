<script lang="ts">
	import GameOfLife from '$lib/assets/GameOfLife.svelte';
</script>

<div class="page">
	<header class="rules">
		<div class="rules-upperleft">
			<ul>
				<h1>- Any live cell with fewer than two live neighbours dies, as if by underpopulation.</h1>
				<h1>- Any live cell with two or three live neighbours lives on to the next generation.</h1>
			</ul>
		</div>
		<div class="rules-upperright">
			<ul>
				<h1>- Any live cell with more than three live neighbours dies, as if by overpopulation.</h1>
				<h1>- Any dead cell with exactly three live neighbours becomes a live cell, as if by reproduction.</h1>
			</ul>
		</div>
	</header>
	<GameOfLife />
</div>

<style>
	.page {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	.rules {
		display: flex;
		justify-content: space-between;
		padding: 20px;
		background: #1900ff;
		color: #333;
	}

	.rules-left, .rules-right {
		flex: 1;
		padding: 0 20px;
	}

	.rules-left {
		text-align: left;
	}

	.rules-right {
		text-align: right;
	}

	ul {
		list-style-type: disc;
		padding-left: 20px;
	}

	h2 {
		margin-top: 0;
	}
</style>
