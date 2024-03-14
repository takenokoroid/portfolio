<script lang="ts">
	import { assets } from '$app/paths';
	import Card from '../bin/components/Card.svelte';
	import ImageCard from '../bin/components/ImageCard.svelte';

	const iconPath = `${assets}/images/nango_square.png`;
</script>

<div>
	<section>
		<img src={iconPath} alt="たけろいどのアイコン" />
		<h2>たけろいど Takeroid</h2>
		<h3>フロントエンドエンジニア / Frontend Engineer</h3>
		<p>
			たけのこの里とSvelteKitが好きな人です。<br
			/>日本のとあるISPでWEBアプリケーションエンジニアとして働いています。
		</p>
	</section>
	<section>
		<Card>
			<p>いつでも探しているよ。どっかに君の姿を</p>
		</Card>
		<Card>
			<p>Twitterをやっているよ</p>
		</Card>
		<ImageCard src={`${assets}/images/sample.jpg`} alt="パスタ" />
		<ImageCard src={`${assets}/images/i_love_svelte.jpg`} alt="私はSvelteが大好きです" />
		<ImageCard src={`${assets}/images/distant_everyday_emories.jpeg`} alt="思い出は遠くの日々" />
		<ImageCard src={`${assets}/images/my_best_memory_on_ff14.png`} alt="一番大事な思い出" />
	</section>
</div>

<footer>
	<p>&copy; 2021-2023 takenokoroid</p>
</footer>

<style>
	img {
		/* imgを丸に切り取る */
		border-radius: 50%;
		/* サイズを小さくする */
		width: 184px;
		height: auto;
		/* 画像をズームする */
		/* 画像の周りに線を引く */
		border: 1px solid #000;
	}
	/* breakpoint 768pxの設定 */
	@media (max-width: 768px) {
		img {
			width: 128px;
		}
	}
</style>
