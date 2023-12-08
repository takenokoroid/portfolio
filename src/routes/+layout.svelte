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
</main>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 1rem;
		position: fixed; /* ヘッダーを固定 */
		top: 0; /* 上端から0の位置に */
		left: 0; /* 左端から0の位置に */
		width: 100%; /* 幅を100%に設定して画面全体に広げる */
		z-index: 1000; /* 他の要素より上に表示する */
	}
	h1 {
		font-size: x-large;
	}
	ul {
		display: flex;
		list-style: none;
	}
	li {
		margin-left: 1rem;
		font-size: medium;
	}
	a {
		text-decoration: none;
		color: #000;
	}
	main {
		padding-left: 13rem; /* 左の余白 */
		padding-right: 13rem; /* 右の余白 */
		padding-top: 12rem;
		padding-bottom: 3rem;
		max-width: 1200px; /* コンテナの最大幅 */
		margin-left: auto; /* 左右中央寄せ */
		margin-right: auto; /* 左右中央寄せ */
	}

	@media (max-width: 768px) {
		main {
			padding-left: 1rem;
			padding-right: 1rem;
		}
	}
</style>
