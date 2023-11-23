<script>
	import { base } from '$app/paths';
	console.log('base:', base);
</script>

<header>
	<h1>
		<a href="{base}/">たけろいど</a>
	</h1>
	<ul>
		<li><a href="{base}/about">ABOUT</a></li>
		<li><a href="{base}/contact">CONTACT</a></li>
	</ul>
</header>
<main>
	base:{base}
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
