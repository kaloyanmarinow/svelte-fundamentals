<script>
	/**
	 * Internal dependencies.
	 */
	import Header from '../../../components/Header.svelte';	
	import Footer from '../../../components/Footer.svelte';	
	import '../../../global.css';

	let name = $state('world');
</script>

<Header />

<div class="section">
	<div class="container">
		<div class="section__title">
			<h2>bind:value</h2>
		</div><!-- /.section__title -->

		<div class="section__box">
			<input bind:value={name} />
			
			<h4>Hello <span>{name}</span>!</h4>
		</div><!-- /.section__box -->
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
		margin-bottom: 30px;
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

	.section .section__box input {
		height: 40px;
		min-width: 300px;
		line-height: 38px;
		background: transparent;
		border: 1px solid rgb(231, 231, 231);
		padding: 0 16px;
		color: rgb(231, 231, 231);
		font-size: 20px;
		transition: border-color .4s;
	}

	.section .section__box input:focus {
		border-color: rgba(165, 207, 39, .7);
	}

	.section .section__box h4 span {
		color: rgb(165, 207, 39);
	}

	.section .section__box > *:not(:last-child) {
		margin-bottom: 30px;
	}
</style>

