<script>
	/**
	* Internal dependencies.
	*/
	import Header from '../components/Header.svelte';	
	import Footer from '../components/Footer.svelte';	
	import '../global.css';
</script>

<Header />

<div class="section">
	<div class="container section__container">
		<div class="section__title">
			<h1>
				Svelte <span>&#123;</span>

				<p>
					<span>&#91;</span> 
					Fundamentals 
					<span>&#93;</span>
				</p>
			</h1>

			<h4>
				&#60;
				Основни примери и функционалности
				&#62;
			</h4>

			<h1>
				<span>&#125;</span>
			</h1>
		</div><!-- /.section__title -->
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

	.section .section__container {
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.section .section__title {
		color: rgb(255, 88, 88);
	}

	.section .section__title span {
		color: #fff;
	}

	.section .section__title h1 p {
		padding-left: 4vw;
		color: rgb(165, 207, 39);
	}

	.section .section__title h4 {
		margin: 40px 0;
		padding-left: 9vw;
	}
</style>