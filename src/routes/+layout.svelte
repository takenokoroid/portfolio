<script>
	import { base } from '$app/paths';

	// 各種ページのパス
	const index = base + '/';
	const about = base + '/about';
	const contact = base + '/contact';
</script>

<header>
	<h1>
		<a href={index}>たけろいど</a>
	</h1>
	<ul>
		<li><a href={about}>ABOUT</a></li>
		<li><a href={contact}>CONTACT</a></li>
	</ul>
</header>
<main>
	<slot />
	<footer>
		<p>&copy; 2021-2023 takenokoroid</p>
	</footer>
</main>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 1rem;
	}
	ul {
		display: flex;
		list-style: none;
	}
	li {
		margin-left: 1rem;
	}
	main {
		padding-left: 200px; /* 左の余白 */
		padding-right: 200px; /* 右の余白 */
		max-width: 1200px; /* コンテナの最大幅 */
		margin-left: auto; /* 左右中央寄せ */
		margin-right: auto; /* 左右中央寄せ */
		height: 1000px;
	}

	@media (max-width: 768px) {
		main {
			padding-left: 0; /* 左の余白をなくす */
			padding-right: 0; /* 右の余白をなくす */
		}
	}
</style>
