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
	}
	ul {
		display: flex;
		list-style: none;
	}
	li {
		margin-left: 1rem;
	}
</style>
