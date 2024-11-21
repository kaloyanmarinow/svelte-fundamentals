<script>
	/**
	 * Internal dependencies.
	 */
	import Header from '../../../components/Header.svelte';	
	import Footer from '../../../components/Footer.svelte';
	import '../../../global.css';

	let size = $state(150);
	let color = $state('#ff3e00');

	let canvas;

	function getRandomColor() {
		return '#' + Math.floor(Math.random() * 16777215).toString(16).padStart(6, '0');
	}

	$effect(() => {
		const context = canvas.getContext('2d');

		context.fillStyle = color;
		context.fillRect(0, 0, size, size);
	});
</script>

<Header />

<div class="section">
	<div class="container">
		<div class="section__title">
			<h2>&#36;effect</h2>
		</div><!-- /.section__title -->

		<div class="section__box">
			<canvas bind:this={canvas} width={size} height={size}></canvas>

			<button 
				class="btn" 
				onclick={() => (color = getRandomColor())}
			>
				Change Color
			</button>
		</div><!-- /.section-box -->
	</div><!-- /.container -->
</div><!-- /.section -->

<Footer />

<style>
	/* Section */
	.section {
		padding: 100px 0;
		display: flex;
		flex-grow: 1;
	}

	.section .section__title {
		color: rgb(255, 88, 88);
		text-align: center;
		margin-bottom: 3rem;
	}

	.section .section__box {
		width: 100%;
		background: rgb(22, 25, 31);
		padding: 40px;
		border-radius: 20px;
		color: rgb(231, 231, 231);
		text-align: center;
		min-height: 300px;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.section .section__box > *:not(:last-child) {
		margin-bottom: 30px;
	}
</style>