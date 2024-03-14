<script>
	import Card from './Card.svelte';
	export let src = '';
	export let alt = '画像の設定がされていません';
	export let linkTitle = '';

	export let href = '';
</script>

<Card>
	<a {href}>
		<div>
			<div>
				<img {src} {alt} />
			</div>
			<div>
				<p>{linkTitle}</p>
				<p>linksub</p>
				<p>いつでもさがしているよ</p>
			</div>
			<div />
		</div>
	</a>
</Card>
