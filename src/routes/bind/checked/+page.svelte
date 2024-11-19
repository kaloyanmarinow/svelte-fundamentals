<script>
	/**
	 * Internal dependencies.
	 */
	import Header from '../../../components/Header.svelte';	
	import Footer from '../../../components/Footer.svelte';
	import '../../../global.css';

	let isChecked = $state(false);
</script>

<Header />

<div class="section">
	<div class="container">
		<div class="section__title">
			<h2>bind:checked</h2>
		</div><!-- /.section__title -->

		<div class="section__box">
			<div class="section__box-input">
				<label>
					<input type="checkbox" bind:checked={isChecked} />

					Yes, I want to join the newletter!
				</label>
			</div><!-- /.section__box-input -->
			
			<div class="section__box-content">
				{#if isChecked}
					<p>
						Thank you. You will receive our emails.
					</p>
				{:else}
					<p>
						You have to subscribe to continue.
					</p>
				{/if}
			</div><!-- /.section__box-content -->
			
			<div class="section__box-actions">
				<button class="btn" disabled={!isChecked}>Subscribe</button>
			</div><!-- /.section__box-actions -->
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

	.section .section__box-input label {
		display: flex;
		gap: 12px;
		align-items: center;
		font-size: 14px;
		position: relative;
	}

	.section .section__box-input label:before {
		content: '';
		display: block;
		width: 12px;
		height: 12px;
		position: absolute;
		top: 4px;
		left: 4px;
		background: rgb(165, 207, 39);
		opacity: 0;
		visibility: hidden;
		transition: opacity .4s, visibility .4s;
	}

	.section .section__box-input input {
		appearance: none;
		background: transparent;
		border: 1px solid rgb(231, 231, 231);
		height: 20px;
		width: 20px;
		transition: border-color .4s;
	}

	.section .section__box-input input:checked {
		border-color: rgb(165, 207, 39);
	}

	.section .section__box-input label:has(input:checked):before {
		opacity: 1;
		visibility: visible;
	}

	.section .section__box > *:not(:last-child) {
		margin-bottom: 30px;
	}
</style>

