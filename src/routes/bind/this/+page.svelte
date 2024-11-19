<script>
	/**
	 * Internal dependencies.
	 */
	import Header from '../../../components/Header.svelte';	
	import Footer from '../../../components/Footer.svelte';	
	import ChildComponent from './ChildComponent.svelte';
	import '../../../global.css';

	let childComponentInstance;

	/**
	 * Call child method.
	 */
	function callChildMethod() {
		if (childComponentInstance) {
			childComponentInstance.sayHello();
		}
	}
</script>

<Header />

<div class="section">
	<div class="container">
		<div class="section__title">
			<h2>bind:this</h2>
		</div><!-- /.section__title -->

		<div class="section__box">
			<ChildComponent bind:this={childComponentInstance} />

			<button class="btn" on:click={callChildMethod}>Call child method</button>
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
</style>

