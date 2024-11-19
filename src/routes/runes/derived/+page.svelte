<script>
	/**
	 * Internal dependencies.
	 */
	import Header from '../../../components/Header.svelte';	
	import Footer from '../../../components/Footer.svelte';
	import '../../../global.css';

	let count = $state(0);	
	let doubled = $derived(count * 2);
</script>

<Header />

<div class="section">
	<div class="container">
		<div class="section__title">
			<h2>&#36;derived</h2>
		</div><!-- /.section__title -->

		<div class="section__box">
			<h4>Clicks Count: {count}</h4>

			<h5>{count} doubled is {doubled}</h5>
			
			<button 
				class="btn" 
				onclick={() => count++}
			>
				Click Here
			</button>
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

	.section .section__box h4 {
		color: rgb(231, 231, 231);
		margin-bottom: 0!important;
	}
</style>
	