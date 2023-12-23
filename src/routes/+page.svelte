<script>
	let currentSection = 0;

	function handleScroll() {
		const scrollY = window.scrollY;
		const sectionHeight = window.innerHeight;
		// 現在のスクロール位置に基づいてセクションを決定する
		currentSection = Math.round(scrollY / sectionHeight);
	}
</script>

<svelte:window on:scroll={handleScroll} />

<div class="sections">
	<section
		class:active={currentSection === 0}
		style="transform: translateX({currentSection === 0 ? 0 : -100}%)"
	>
		Hello. There's nothing here "yet".
	</section>
	<section
		class:active={currentSection === 1}
		style="transform: translateX({currentSection === 1 ? 0 : -100}%)"
	>
		It's really not there!
	</section>
	<!-- 追加のセクションがあればここに -->
</div>

<footer>
	<p>&copy; 2021-2023 takenokoroid</p>
</footer>

<style>
	.sections {
		height: 200vh; /* セクションの数に応じて調整する */
		overflow-x: hidden;
	}
	section {
		min-height: 100vh;
		width: 100vw;
		position: fixed;
		transition: transform 1s ease-out;
	}
	.active {
		/* アクティブなセクションのスタイル */
	}
	footer {
		display: flex;
		justify-content: center;
		align-items: center;
		padding: 1rem;
		position: fixed; /* ヘッダーを固定 */
		bottom: 0; /* 画面の下端に */
		left: 0; /* 画面の左端に */
		width: auto; /* フッターの内容に合わせて幅を調整 */
	}
</style>
