<script>
	import Card from './Card.svelte';
	export let src = '';
	export let alt = '画像の設定がされていません';
</script>

<Card>
	<img class="image" {src} {alt} />
</Card>

<style>
	.image {
		/* 画像を丸に切り取る */
		border-radius: inherit;
		/* 画像の幅 */
		width: 100%;
		/* 画像の高さ */
		height: auto;
	}
</style>
