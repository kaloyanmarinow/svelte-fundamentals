<script>
	/**
	 * Internal dependencies.
	 */
	import Header from '../../../components/Header.svelte';	
	import Footer from '../../../components/Footer.svelte';	
	import '../../../global.css';

	/**
	 * External dependencies.
	 */	
	import { onMount } from 'svelte';

	let photos = [];

	onMount(async () => {
		const res = await fetch(`https://reqres.in/api/users?delay=3`);
		const resJSON = await res.json();
		photos = resJSON.data;
	});
</script>

<Header />

<div class="section">
	<div class="container">
		<div class="section__title">
			<h2>onMount()</h2>
		</div><!-- /.section__title -->

		<div class="section__box">
			<ul class="section__box-list">
				{#each photos as photo}
					<li>
						<img src={photo.avatar} alt={photo.title}>
					</li>
				{:else}
					<h4>Loading...</h4>
				{/each}
			</ul><!-- /.section__box-list -->
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

	.section .section__box-list {
		text-align: center;
		list-style-type: none;
		display: grid;
		justify-content: center;
		grid-template-columns: repeat(6, 10rem);
		gap: 16px;
	}

	.section .section__box-list h4 {
		grid-column: 1 / -1;
	}

	.section .section__box-list li {
		position: relative;
		aspect-ratio: 1 / 1;
	}

	.section .section__box-list li img {
		object-fit: cover;
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
	}
</style>