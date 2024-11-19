<script>
	let props = $props();
</script>

<div class="section">
	<div class="container">
		<div class="section__title">
			<h2>&#36;props</h2>
		</div><!-- /.section__title -->

		<div class="section__box">
			<h2>
				This component is <span>{props.adjective}</span>!
			</h2>
		</div><!-- /.section__box -->
	</div><!-- /.container -->
</div><!-- /.section -->

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

	.section .section__box h2 span {
		color: rgb(165, 207, 39);
	}
</style>