<script lang="ts">
	import { assets } from '$app/paths';

	const iconPath = assets + '/nango_square.png';
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
		<div class="card"><p>いつでも探しているよどっかに君の姿を</p></div>
		<div class="card"><p>Twitterをやっているよ</p></div>
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
	.card {
		/* カードの背景色 */
		background-color: #fff;
		/* カードの幅 */
		width: 100%;
		/* カードの高さ */
		height: 100px;
		/* カードの角丸 */
		border-radius: 10px;
		/* カードの影 */
		box-shadow: 0 0 2px rgba(0, 0, 0, 0.5);
		/* カードの中の文字の位置 */
		text-align: center;
		/* カードの中の文字の位置 */
		line-height: 100px;
		/* カードの中の文字の大きさ */
		font-size: 20px;
	}
</style>
