<div class="card">
	<slot />
</div>

<style>
	.card {
		/* カードの背景色 */
		background-color: #fff;
		/* カードの幅 */
		width: 100%;
		/* カードの高さ */
		height: auto;
		/* カードの角丸 */
		border-radius: 20px;
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
